<template>
    <section class="recipes">
        <Recipe
        thumbnail="https://static.pexels.com/photos/2232/vegetables-italian-pizza-restaurant.jpg"
        title="Delicious Pizza"
        previewText="Awesome Pizza!" />
        <Recipe
        thumbnail="https://static.pexels.com/photos/37405/food-prawn-asian.jpg"
        title="Sea Food Salad"
        previewText="Very tasty indeed!" />
    </section>
</template>
<script>
import Recipe from "@/components/Recipe"
export default {
  components: {
    Recipe
  }
}
</script>
<style scoped>
.recipes{
display: flex;
flex-flow: row wrap;
justify-content: center;
align-items: center;
}
</style>

