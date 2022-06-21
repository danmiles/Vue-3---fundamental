<template>
    <form class="form" @submit.prevent>
        <h4 class="form__title">Create a post</h4>

        <input
            v-model="post.title"
            class="input"
            type="text"
            placeholder="Post title"
        />
        <input
            v-model="post.body"
            class="input"
            type="text"
            placeholder="Post description"
        />
        <button class="btn" @click="createPost">New post</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            post: {
                title: "",
                body: "",
                mody: "",
            },
        };
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit("create", this.post);
            this.post = {
                title: "",
                body: "",
            };
        },
    },
};
</script>

<style></style>
