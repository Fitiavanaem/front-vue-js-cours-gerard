<script>
import BlogList from './components/BlogList.vue';
export default {
  name: "App",
  components: {
    BlogList
  },
  data() {
    return {
      Posts: [
        {
          id: 1,
          tilte: "Poste 1",
          contenent: "Lore uidem  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam.nemo itaque nequecumque inventore maiores esse architecto rem nulla consequuntur,modi corrupti ddoloro",
          date: "01-03-2023",
          auteur: "Fitiavana"
        },
        {
          id: 2,
          tilte: "Poste 2",
          contenent: "Lore uidem  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam.nemo itaque nequecumque inventore maiores esse architecto rem nulla consequuntur,modi corrupti ddoloro",
          date: "01-03-2021",
          auteur: "Roschtand"
        },
        {
          id: 3,
          tilte: "Poste 3",
          contenent: "Lore uidem  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Minima omnis repellat, possimus maiores consectetur perferendis cupiditate molestiae necessitatibus numquam saepe illo ratione eaque, sit rem quia officiis explicabo, vero veniam.nemo itaque nequecumque inventore maiores esse architecto rem nulla consequuntur,modi corrupti ddoloro",
          date: "19-03-2020",
          auteur: "Bema"
        }
      ]
    }
  },
  emits: [
    'delete-post'
  ],
  methods: {
    deleteFonction(id) {
      let indexToDelete = this.Posts.findIndex(post => post.id === id);
      if (indexToDelete !== -1) {
        this.Posts.splice(indexToDelete, 1);
      }
      console.log(this.Posts);
    },

  }
}
</script>
<template>
  <div>
    <!-- <BlogPost :PostTitle="post.tilte"
              :PostContent="post.contenent"
              :PostDate="post.date" 
              :PostAuteur="post.auteur"
              v-for="post in Posts" :key="post.id"
              >
    </BlogPost> -->
    <BlogList :Posts="Posts" @delete-post="deleteFonction"></BlogList>

  </div>
</template>
<style scoped ></style>