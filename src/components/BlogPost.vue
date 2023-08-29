<script>

export default {
    name: "BlogPost",
    data() {
        return {
            Auteur: "Fitiavana",
            PostuleDate: "19-03-2023"
        }
    },
    props: {
        post: {
            type: Object,
            required: true
        }
    },
    methods: {
        deletePost() {
            console.log("Bonjour");
        }
    }
}
</script>
<template>
    <div>
        <h1>{{ post.title }}</h1>
        <p>{{ post.contenent }}</p>
        <div class="post_info">
            <h4>Publié le {{ post.date }}</h4>
            <h4>Auteur :{{ post.auteur }}</h4>
            <button class="button" @click="$emit('delete-post', post.id)">Supprimer</button>
        </div>
    </div>
</template>
<style scoped>
.post_info {
    text-align: right;
    margin-top: 3rem;
}

p {
    text-align: justify;
}

.button {
    background-color: rgb(238, 61, 29);
    border: none;
    color: white;
    padding: 0.6rem;
    border-radius: 0.4rem;
    text-size-adjust: 3px;
    cursor: pointer;
}
</style>