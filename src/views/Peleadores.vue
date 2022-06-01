<template>
  <div class="flex flex-col items-center">
    <h1 class="text-2xl mb-4">Listado de peleadores</h1>
    <div class="w-48 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg dark:bg-gray-700 dark:border-gray-600 dark:text-white">
        <router-link 
            v-for="peleador in peleadores" :key="peleador.id"
            :to="`/peleadores/${peleador.id}`" 
            class="block w-full px-4 py-2 border-b border-gray-200 cursor-pointer hover:bg-gray-100 hover:text-blue-700 dark:border-gray-600 dark:hover:bg-gray-600 dark:hover:text-white dark:focus:ring-gray-500 dark:focus:text-white text-center">
            {{ peleador.nombre }}
        </router-link>
    </div>
  </div>
</template>

<script>
export default {
    data: () => ({
        peleadores: [],
    }),
    created() {
        fetch('/peleadores.json').then((res) => res.json()).then((data) => {
            this.peleadores = data
        })
    }
}
</script>

<style>

</style>