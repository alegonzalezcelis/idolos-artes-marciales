<template>
    <div class="text-sm font-medium text-center text-gray-500 border-b border-gray-200 dark:text-gray-400 dark:border-gray-700 mb-8">
      <ul class="flex flex-wrap -mb-px">
        <li class="mr-2">
          <a class="inline-block p-4 rounded-t-lg border-b-2 border-transparent hover:text-blue-600 hover:border-blue-600">
            <router-link to="/">Home</router-link>
          </a>
        </li>
        <li class="mr-2">
          <a class="inline-block p-4 rounded-t-lg border-b-2 border-transparent hover:text-blue-600 hover:border-blue-600" aria-current="page">
            <router-link to="/peleadores">Peleadores</router-link>
          </a>
        </li>
        <li class="mr-2">
          <a href="#" class="inline-block p-4 rounded-t-lg border-b-2 border-transparent hover:text-blue-600 hover:border-blue-600">
            <router-link to="/buscador">Buscador</router-link>
          </a>
        </li>
      </ul>
    </div>
</template>