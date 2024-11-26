<script setup>
import BookList from './components/BookList.vue'
import BookCards from './components/BookCards.vue'
import books from '@/bookdata';
import { ref } from 'vue';

const isCardView = ref(false)
let toggleView = () => isCardView.value = !isCardView.value
</script>

<template>
  <div class="container-fluid">
    <button type="button" class="btn btn-primary" @click="toggleView">
      <span v-if="!isCardView">Cards</span>
      <span v-else>Table view</span>
    </button>

    <BookList v-if="!isCardView" :books="books" />
    <BookCards v-if="isCardView" :books="books" />

  </div>
</template>

<style scoped>
div {
  margin: 10px;
}
</style>
