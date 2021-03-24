<template>
  <div class="w-1/2 mx-auto my-20">
      <h1 class="text-3xl font-semibold text-red-600">
          {{tituloBlog}}
      </h1>
      <article class="my-20 text-gray-600">
          <h2 class="text-5xl font-semibold mb-5">Titulo do Artigo</h2>
          <p class="mb-5">Resumo do Artigo</p>
          <p class="text-red-500">Ler Mais</p>
      </article>
  </div>
</template>

<script>
export default {
    data(){
        return {
            tituloBlog: "Super Blog"
        }
    } 
}
</script>
