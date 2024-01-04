<script setup>
import { ref } from 'vue'
import ShoppingList from './ShoppingList.vue'
const items = ref([])
const newItem = ref("")


const props = defineProps([''])
</script>

<template>
<ul>
    <li v-for="item in items" :key="id">{{item}}</li>
</ul>

<form class="addItemForm">
<button v-on:submit="items.push({id: items.length +1, newItem})" class="btn btn-primary">
    Save item
  </button> 
</form>

</template>