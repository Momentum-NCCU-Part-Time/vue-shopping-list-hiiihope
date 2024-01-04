<script setup>
import { ref } from 'vue'
// import NewForm from './NewForm.vue'
import shoppingItems from './ShoppingItems.vue'
// import NewList from './NewList.vue'
const lists = ref([])
const purchased = ref(false)

fetch('http://localhost:3000/lists/', {
  method: 'GET',
  headers: { 'Content-type': 'application/json' }
})
  .then((res) => res.json())
  .then((data) => (lists.value = data))

const getLists = () => {
  fetch('http://localhost:3000/lists/', {
    method: 'GET',
    headers: { 'Content-type': 'application/json' }
  })
    .then((res) => res.json())
    .then((data) => (lists.value = data))
}
</script>

<template>
  <input v-model="newItem" v-on:keyup.enter=""  type="text" placeholder="Add an item" />
  <!-- <button class="btn btn-primary">
    Save item
  </button>   -->
  <!-- push new
/* button,  -->
</template>
