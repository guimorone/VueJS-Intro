<template>
    <div>
        <b-col>
            <b-card 
            :title="nome"
            img-src="https://picsum.photos/600/300?image=25"
            img-alt="Curso de VUE.JS"
            style="max-width:20rem"
            class="mb-2"
            border-variant="primary"
            header="Curso"
            header-bg-variant="primary"
            header-text-variant="white"
            align="center">
                <b-card-text>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin mauris tellus, pulvinar in risus in, semper placerat purus. Phasellus hendrerit.
                </b-card-text>
                <b-button variant="primary">Comprar</b-button>
            </b-card>
        </b-col>
    </div>
</template>
<script>

    export default {
        props: {
            nome: {
                type: String,
                required: true
            }
        },
    };

</script>