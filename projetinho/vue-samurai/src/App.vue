<template>
  <div id="app">
    <Header class="mb-5"/>
    <b-container>
      <b-row align-v="center">
        <Card v-for="curso in cursos" :key="curso.id" :nome="curso.name"/>
      </b-row>
    </b-container>
  </div>
  
</template>

<script>
import Card from './components/Card.vue';
import Header from './components/Header.vue';

export default {
  name: 'App',
  data() {
    return {
      cursos: []
    }
  },
  components: {
    Card,
    Header
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      const res = await fetch("cursos.json");
      const val = await res.json();
      this.cursos = val.dados;
      console.log(val.dados);
    }
  }
}
</script>
