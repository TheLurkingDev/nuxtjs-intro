<template>
    <section class="recipes">
        <Recipe 
            v-for="recipe in recipes"
            :key="recipe.id"
            :thumbnail="recipe.thumbnail"
            :title="recipe.title"
            :id="recipe.id"
            :previewText="recipe.previewText"
        />
    </section>
</template>

<script>
import Recipe from '@/components/Recipe';

export default {
    components: { // Register the Recipe component.
        Recipe
    },
    asyncData() { // Loaded from server on initial fetch.
        // Could use an axios call here: return axios.get()
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipes: [
                        {
                            id: "1",
                            title: "Chic Fil' A",
                            previewText: "Delicious chicken sandwich.",
                            thumbnail: "https://imagesvc.timeincapp.com/v3/mm/image?url=https%3A%2F%2Fcdn-image.foodandwine.com%2Fsites%2Fdefault%2Ffiles%2Fstyles%2Fmedium_2x%2Fpublic%2F1519844002%2Ffast-food-mobile-apps-chick-fil-a-FT-BLOG0218.jpg%3Fitok%3D7d_gu0JA&w=800&q=85"
                        },
                        {
                            id: "2",
                            title: "Vege-burger",
                            previewText: "From Red Robin no less.",
                            thumbnail: "https://amp.businessinsider.com/images/5a7dc169d03072af008b4bf2-750-562.jpg"
                        }
                    ]
                })
            }, 1500);
        });
    }
}
</script>


<style scoped>
    .recipes {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: center;
    }
</style>