<template>
  <div id="app" class="container mx-auto flex flex-col items-center">
    <Navbar></Navbar>
    <router-view />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
export default {
    data: () => ({}),
    methods: {},
    components: { Navbar }
}
</script>