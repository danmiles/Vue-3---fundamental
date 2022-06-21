<template>
    <div class="container">

        <post-form 
            @create="createPost"
        />
        
        <post-list 
            :posts="posts"
        />

    </div>
</template>

<script>

import PostForm from "@/components/PostForm";

import PostList from "@/components/PostList";

export default {
    components: {
        PostList, PostForm
    },
    data() {
        return {
            posts: [
                { id: 1, title: "Javascript-1", body: "Post description 1" },
                { id: 2, title: "Javascript-2", body: "Post description 2" },
                { id: 3, title: "Javascript-3", body: "Post description 3" },
                { id: 4, title: "Javascript-3", body: "Post description 4" },
            ],
        };
    },
    methods: {
        createPost (post) {
            this.posts.push(post)
        }
    }
};
</script>

<style>
@import "/src/style.css";
</style>
