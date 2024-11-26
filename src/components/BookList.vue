<script setup>
import { ref } from 'vue';
const props = defineProps(['books'])
</script>

<template>
    <table class="table">
        <thead>
            <tr>
                <th scope="col">Author</th>
                <th scope="col">Title</th>
                <th scope="col">Description</th>
                <th scope="col">Image</th>
            </tr>
        </thead>
        <tbody v-for="book in props.books">

            <tr>
                <td>{{ book.author }}</td>
                <td>{{ book.title }}</td>
                <td>{{ book.description }}</td>
                <td><img :src=book.img_url alt=""></td>
            </tr>
        </tbody>
    </table>
</template>


<style scoped>
img {
    width: 200px;
    height: 100px;
}
</style>