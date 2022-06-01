<template>
  <div class="flex flex-col items-center">
    <h1 class="text-2xl mb-4">Buscador de peleadores</h1>
    <form @submit.prevent="handleSubmit">
        <div class="flex flex-col items-center">
            <div class="p-4 mb-4 text-sm text-blue-700 bg-blue-100 rounded-lg dark:bg-blue-200 dark:text-blue-800 w-full" role="alert">Busca un personaje por su <span class="font-bold">número de id</span>
            </div>
            <input 
                type="number"
                placeholder="Ejemplo: 4" 
                v-model="idBuscar"
                min="1"
                max="5"
                class="w-full p-2 text-gray-900 border border-gray-300 rounded-lg bg-gray-50 sm:text-xs focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500">
        </div>
        <button type="submit" class="text-white bg-blue-700 hover:bg-blue-800 focus:outline-none focus:ring-4 focus:ring-blue-300 font-medium rounded-full text-sm px-5 py-2.5 text-center mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 mt-5 w-full">Buscar</button>

    </form>
  </div>
</template>

<script>
export default {
    data: () => ({
        idBuscar: '',
    }),
    methods: {
        handleSubmit(){
            console.log(this.idBuscar)
            this.$router.push(`/peleadores/${this.idBuscar}`)
        }
    }
};
</script>

<style></style>
