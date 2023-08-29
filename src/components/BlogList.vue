<script>
import BlogPost from './BlogPost.vue';
export default {
    name: "BlogList",
    components: {
        BlogPost
    },
    props: {
        Posts: {
            type: Array,
            required: true
        }
    },
    emits: [
        'delete-post'
    ]
}
</script>
<template>
    <div>
        <BlogPost :post="post" v-for="post in Posts" :key="post.id" @delete-post="$emit('delete-post', post.id)">
        </BlogPost>
    </div>
</template>
<style scoped></style>