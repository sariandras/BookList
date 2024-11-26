<template>
    <div class="row">
        <div class="card col-md-4 col-lg-4 col-sm-6 mx-2 my-2" style="width: 24rem;" v-for="book in props.books">
            <img :src=book.img_url class="card-img-top">
            <div class="card-body">
                <h4 class="card-title">{{ book.title }}</h4>
                <h5 class="card-title">{{ book.author }}</h5>
                <p class="card-text">{{ book.description }}</p>
            </div>
        </div>
    </div>

</template>

<script setup>
const props = defineProps(['books'])

</script>

<style lang="scss" scoped></style>