<template>
    <section class="recipes">
        <article class="recipe">
            <div class="thumbnail" style="background-image: url('https://imagesvc.timeincapp.com/v3/mm/image?url=https%3A%2F%2Fcdn-image.foodandwine.com%2Fsites%2Fdefault%2Ffiles%2Fstyles%2Fmedium_2x%2Fpublic%2F1519844002%2Ffast-food-mobile-apps-chick-fil-a-FT-BLOG0218.jpg%3Fitok%3D7d_gu0JA&w=800&q=85')"></div>
            <h1>Title</h1>
            <p>Some nice preview text.</p>            
        </article>
        <article class="recipe">
            <div class="thumbnail" style="background-image: url('https://amp.businessinsider.com/images/5a7dc169d03072af008b4bf2-750-562.jpg')"></div>
            <h1>Title</h1>
            <p>Some nice preview text.</p>            
        </article>
    </section>
</template>

<style scoped>
    .recipes {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: center;
    }
    
    .recipe {
        box-sizing: border-box;
        width: 280px;
        padding: 8px;
        border: 1px solid #ccc;
        box-shadow: 0 2px 2px #aaa;
        margin: 10px;
    }

    .thumbnail {
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 200px;
    }
</style>