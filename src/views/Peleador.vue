<template>
  <div>
    <div v-if="peleador" class="max-w-sm bg-white rounded-lg border border-gray-200 shadow-md dark:bg-gray-800 dark:border-gray-700">
        <img class="rounded-t-lg" :src="peleador.imgSrc" alt="" />
        <div class="p-5">
            <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
                {{ peleador.nombre }}
            </h5>
            <p class="mb-3 mt-5 font-normal text-gray-700 dark:text-gray-400">{{ peleador.description }}</p>
            <div class="rounded-full h-5 w-5 p-5 text-white font-bold flex items-center justify-center bg-blue-700 mx-auto ">{{ $route.params.id }}</div>
    </div>
</div>    
    <div v-if="!peleador">
      <h1>No se pudo encontrar el peleador</h1>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    peleador: { nombre: "", imgSrc: "" },
  }),
  created() {
    fetch("/peleadores.json")
      .then((response) => response.json())
      .then((peleadores) => {
        this.peleador =
          peleadores.find(
            (peleador) => peleador.id === this.$route.params.id
          ) || null;
      });
  },
};
</script>

<style></style>
