<template>
    <section>
        <div class="main-info">
            <img :src="require('@/assets/img/main-photo.webp')" alt="main-photo">
            <div class="main-info__article">
                <h3 class="main-info__article_title">Articles & News</h3>
                <div class="main-info__article_links">
                    <a href="#">Home</a>
                    <a href="#">Blog</a>
                </div>
            </div>
        </div>
    </section>
    <section>
        <router-link to="/blog/details">
            <div class="post center">
                <h2 class="post__heading">Latest Post</h2>
                <div class="post-box">
                    <img :src="require('@/assets/img/post-photo.webp')" alt="post-photo">
                    <div class="post-box__description">
                        <h3 class="post-box__description_title">Low Cost Latest Invented Interior Designing Ideas</h3>
                        <p class="post-box__description_upper-text">Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem
                            vitae
                            turpis dignissim maximus.posuere
                            in.Contrary to popular belief.</p>

                        <p class="post-box__description_down-text">Lorem Ipsum is not simply random text. It has roots in a
                            piece of
                            classica.</p>
                        <p class="post-box__description_date">
                            26 December,2022
                        </p>
                    </div>
                </div>

            </div>
        </router-link>

    </section>
    <section>
        <div class="arcticles-heading center">Articles & News</div>
        <div class="down-articles">
            <div class="down-articles__card" v-for="article in articles" :key="article.id">
                <router-link to="./blog/details">
                    <img class="down-articles__img" :src="article.img" :alt="article.id">
                    <h3 class="down-articles__card_title">{{ article.heading }}</h3>
                    <p class="down-articles__card_date">{{ article.date }} </p>
                    <svg class="down-articles__card_activator" width="52" height="53" viewBox="0 0 52 53" fill="none"
                        xmlns="http://www.w3.org/2000/svg">
                        <circle cx="26" cy="26.267" r="26" fill="#F4F0EC" />
                        <path d="M23.7714 32.9527L29.7143 26.267L23.7714 19.5813" stroke="#292F36" stroke-width="2"
                            stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                </router-link>


            </div>
        </div>

        <div class="page">
            <a href="#" class="page-links">
                <svg width="53" height="52" viewBox="0 0 53 52" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
                    <text x="17" y="31" font-family="Jost" font-size="16" font-weight=500 fill="black">01</text>
                </svg>
            </a>
            <a href="#" class="page-links"> <svg width="53" height="52" viewBox="0 0 53 52" fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
                    <text x="17" y="31" font-family="Jost" font-size="16" font-weight=500 fill="black">02</text>
                </svg>
            </a>
            <a href="#" class="page-links">
                <svg width="53" height="52" viewBox="0 0 53 52" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
                    <text x="17" y="31" font-family="Jost" font-size="16" font-weight=500 fill="black">03</text>
                </svg>
            </a>
            <a href="#" class="page-links">
                <svg width="53" height="52" viewBox="0 0 53 52" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
                    <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round" />
                </svg>

            </a>



        </div>
    </section>
</template>

<script>
export default {
    name: 'BlogContentComp',

    data() {
        return {
            articles: [
                {
                    id: 1,
                    img: require('@/assets/img/articles/Image1.webp'),
                    heading: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                },
                {
                    id: 2,
                    img: require('@/assets/img/articles/Image2.webp'),
                    heading: 'Low Cost Latest Invented Interior Designing Ideas.',
                    date: '22 December,2022',
                },
                {
                    id: 3,
                    img: require('@/assets/img/articles/Image3.webp'),
                    heading: 'Best For Any Office & Business Interior Solution',
                    date: '25 December,2022',
                },
                {
                    id: 4,
                    img: require('@/assets/img/articles/Image4.webp'),
                    heading: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                },
                {
                    id: 5,
                    img: require('@/assets/img/articles/Image5.webp'),
                    heading: 'Low Cost Latest Invented Interior Designing Ideas.',
                    date: '22 December,2022',
                },
                {
                    id: 6,
                    img: require('@/assets/img/articles/Image6.webp'),
                    heading: 'Best For Any Office & Business Interior Solution',
                    date: '25 December,2022',
                }
            ]
        };
    },
};
</script>

<style scoped>
.main-info {
    display: flex;
    justify-content: center;
}

.main-info img {
    position: relative;
}

.main-info__article {
    position: absolute;
    top: 294px;
    border-radius: 37px 37px 0px 0px;
    background: #FFF;
    display: flex;
    padding: 41px 78px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
}

.main-info__article_title {
    color: #292F36;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
}

.main-info__article_links {
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.22px;
}

.main-info__article a:not(:last-child)::after {
    content: " /";
    margin-right: 5px;
}

.main-info__article a {
    color: #4D5053;
}

.post {
    margin-top: 150px;
    margin-bottom: 150px;
}

.post__heading {
    margin-bottom: 27px;
    color: #292F36;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 1px;
}

.post-box {
    display: flex;
    justify-content: center;
    gap: 65px;
}

.post-box img {
    border-radius: 65px;
}

.post-box__description {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.post-box__description_title {
    margin-bottom: 22px;
    color: #292F36;
    font-family: DM Serif Display;
    font-size: 25px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 0.5px;
}

.post-box__description p {
    color: #4D5053;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.22px;
}

.post-box__description_upper-text {
    margin-bottom: 40px;
}

.post-box__description_down-text {
    margin-bottom: 41px;
}



.down-articles {
    display: flex;
    justify-content: center;
    gap: 27px;
    display: grid;
    grid-template-columns: repeat(3, 382px);
}

.down-articles__img {
    border-radius: 40px 40px 0 0;
}

.down-articles__card {
    padding: 21px;
    border-radius: 62px;
    border: 1px solid #E7E7E7;
    background: #FFFFFF;
    box-shadow: 0px 10px 30px 0px rgba(255, 255, 255, 0.25);
    max-width: 382px;
    position: relative;
}

.down-articles__card:hover {
    background: #F4F0EC;
    transition: 0.5s;
}

.down-articles__card:hover circle {
    fill: #fff;
}

.down-articles__card_title {
    padding-top: 21px;
    padding-bottom: 30px;
    color: #292F36;
    font-family: DM Serif Display;
    font-size: 25px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 0.5px;
    max-width: 305px;
}

.down-articles__card_date {
    padding-bottom: 21px;
    color: #4D5053;
    font-family: Jost;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    letter-spacing: 0.16px;
    text-transform: capitalize;
}

.down-articles__card_activator {
    position: absolute;
    bottom: 27px;
    right: 21px;
}

.arcticles-heading {
    margin-bottom: 30px;
    color: #292F36;
    font-family: DM Serif Display;
    font-size: 50px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    letter-spacing: 1px;
}

.page {
    margin-top: 51px;
    margin-bottom: 200px;
    display: flex;
    justify-content: center;
    gap: 20px;
}
</style>