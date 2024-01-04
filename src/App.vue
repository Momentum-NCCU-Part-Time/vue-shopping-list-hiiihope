<script setup>
import { ref } from 'vue'
import ShoppingLists from './components/ShoppingList.vue'
import ShoppingItems from './components/ShoppingItems.vue';

const header = ref('Shopping List')

</script>

<template>
  <div id="header">
    <h1>{{ header }}</h1>
    
  </div>

  <div class="mainPage">
  
  </div>
  <ShoppingLists/>
  <ShoppingItems/>
  
</template>

<style scoped></style>

