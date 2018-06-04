<template>
  <section class="recipes">
    <Recipe 
    v-for="recipe in recipes" :key="recipe.id"
    :thumbnail="recipe.thumbnail" 
    :title="recipe.title"
      :id="recipe.id" 
      :previewText="recipe.previewText"
       />

  </section>
</template>
<script>
import Recipe from "@/components/Recipe"
export default {
  components: {
    Recipe
  },
  asyncData(){
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: "1",
              title: "Delicious Pizza!",
              previewText: "Awesome Pizza!",
              thumbnail: "https://static.pexels.com/photos/2232/vegetables-italian-pizza-restaurant.jpg"
            },
            {
              id: "2",
              title: "Sea Food Salad",
              previewText: "Very tasty indeed!",
              thumbnail: "https://static.pexels.com/photos/37405/food-prawn-asian.jpg"
            }
          ]
        })
      }, 1500)
    })
  }
};
</script>
<style scoped>
  .recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    padding: 30px;
  }
</style>