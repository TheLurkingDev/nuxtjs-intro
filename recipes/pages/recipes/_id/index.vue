<template>
    <section class="single-recipe">
        <h1>{{ recipe.title }}</h1>
        <div>
            <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
        </div>
        <p>{{ recipe.description }}</p>        
    </section>
</template>

<script>
export default {
    asyncData(context) {         
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipe: [
                        {
                            id: "1",
                            title: "Chic Fil' A",
                            previewText: "Delicious chicken sandwich.",
                            description: "Amazingly delicious. Very good indeed. You must try!",
                            thumbnail: "https://imagesvc.timeincapp.com/v3/mm/image?url=https%3A%2F%2Fcdn-image.foodandwine.com%2Fsites%2Fdefault%2Ffiles%2Fstyles%2Fmedium_2x%2Fpublic%2F1519844002%2Ffast-food-mobile-apps-chick-fil-a-FT-BLOG0218.jpg%3Fitok%3D7d_gu0JA&w=800&q=85"
                        },
                        {
                            id: "2",
                            title: "Vege-burger",
                            previewText: "From Red Robin no less.",
                            description: "Amazingly delicious. Very good indeed. You must try!",
                            thumbnail: "https://amp.businessinsider.com/images/5a7dc169d03072af008b4bf2-750-562.jpg"
                        }
                    ].find(obj => obj.id === context.params.id)
                })
            }, 1500);
        });
    }
}
</script>


<style scoped>
    .single-recipe {
        display: flex;
        flex-flow: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 30px;
    }

    .recipe-image {
        width: 100%;
    }
</style>