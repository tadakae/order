<!-- App.vue -->
<template>
  <div id="app">
    <MenuItems />
  </div>
</template>

<script>
import MenuItems from './components/MenuItems.vue';

export default {
  name: 'App',
  components: {
    MenuItems
  }
};
</script>

<style>
/* Глобальные стили, если необходимы */
</style>