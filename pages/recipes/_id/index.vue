<template>
    <section class="single-recipe">
        <h1>{{ recipe.title }}</h1>
        <div>
            <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
        </div>
        <p>{{ recipe.descriptionText }}</p>
    </section>
</template>
 
<script>
    export default {
 asyncData(context){
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Delicious Pizza!",
              previewText: "Awesome Pizza!",
              descriptionText: "This is really a delicious meal!",
              thumbnail: "https://static.pexels.com/photos/2232/vegetables-italian-pizza-restaurant.jpg"
            },
            {
              id: "2",
              title: "Sea Food Salad",
              previewText: "Very tasty indeed!",
              descriptionText: "This is really a delicious meal!",
              thumbnail: "https://static.pexels.com/photos/37405/food-prawn-asian.jpg"
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.single-recipe{
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
}
.recipe-image{
    width: 50%;
}
</style>