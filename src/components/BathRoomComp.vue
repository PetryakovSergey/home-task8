<template>
    <div class="products center">
        <div class="products__card" v-for="(bathroom, index) in bathrooms" :key="index">
            <img :src="bathroom.imgUrl" alt="photo1">
            <router-link to="project/details">
                <div class="description-box">
                    <div class="description">
                        <h3 class="description__title">{{ bathroom.title }}</h3>
                        <p class="description__section">{{ link }}</p>
                    </div>
                    <svg width="70" height="70" viewBox="0 0 70 70" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="35" cy="35" r="35" fill="#F4F0EC" />
                        <path d="M32 44L40 35L32 26" stroke="#292F36" stroke-width="2" stroke-linecap="round"
                            stroke-linejoin="round" />
                    </svg>
                </div>
            </router-link>


        </div>
    </div>
</template>

<script>


export default {
    name: 'BathRoomComp',

    data() {
        return {
            bathrooms: [
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom1.webp`),
                    title: 'Minimal Bathroom',

                },
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom2.webp`),
                    title: 'Minimal Bathroom',

                },
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom3.webp`),
                    title: 'Classic Minimal Bathroom',

                },
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom4.webp`),
                    title: 'Modern Bathroom',

                },
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom5.webp`),
                    title: 'Minimal Bathroom table',

                },
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom6.webp`),
                    title: 'System Table',

                },
                {
                    imgUrl: require(`../assets/img/bedrooms/bedroom7.webp`),
                    title: 'Modern Bathroom',

                },
            ],
            link: 'Decor / Architecture'
        };
    },

};
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
}

a {
    text-decoration: none;
}

.center {
    padding-left: calc(50% - 600px);
    padding-right: calc(50% - 600px);
}

.products {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-gap: 10px;
    grid-auto-flow: dense;
}

.description-box {
    cursor: pointer;
}


.products__card:hover circle {
    transition: 0.5s;
    fill: #fff;
}
</style>