<template>
    <div class="post" v-for="post in posts">
        <h2><strong>Name:</strong> {{ post.title }}</h2>
        <p><strong>Description:</strong> {{ post.body }}</p>
    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>

<style>

</style>