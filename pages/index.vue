<template>
  <div class="w-1/2 mx-auto my-20">
    <button 
        class="bg-red-500 p-3 text-white"
        v-on:click="carregarListaArtigos()"
    >
        Carrregar artigos
    </button>
      <h1 class="text-3xl font-semibold text-red-600">
          {{tituloBlog}}
      </h1>
      <article v-for="artigo in listaArtigos" class="my-20 text-gray-600">
          <h2 class="text-5xl font-semibold mb-5">{{artigo.titulo}}</h2>
          <p class="mb-5">{{artigo.resumo}}</p>
          <p class="text-red-500">Ler Mais</p>
      </article>
  </div>
</template>

<script>
export default {
    data(){
        return {
            listaArtigos: [],
            tituloBlog: "Super Blog"
        }
    },
    methods:{
         carregarListaArtigos() {
              this.$axios
                .$get("https://api.pistonapi.com/soper-blog/artigo")
                .then((respostaAPI) => {
                    this.listaArtigos = respostaAPI.data;
                });
        },
    }
}
</script>
