<template>
    <section class="header">
        <div class="header__title">
            <h1>{{ title }}</h1>
            <p>{{ description }}</p>
        </div>

        <div class="header__image">
            <img :src="image" alt="">
        </div>
        
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Bugs Tracker',
            description: 'The board for only fun, no offence',
            image: '',
        }
    },

    created() {
        this.fetchImage();
    },

    methods: {
        async fetchImage() {
            const imageUrl = 'https://randomuser.me/api';
            const res = await fetch(imageUrl);
            const { results } = await res.json();
            this.image = results[0].picture.large;
        }
    }
}
</script>

<style>
    .header {
        display: grid;
        grid-template-columns: repeat(10, 1fr);
        column-gap: var(--gap-big);
        margin-top: var(--top-small);
    }

    .header__title {
        grid-column: 1/ span 4;
    }

    .header__title h1 {
        font-size: var(--heading);
        margin-bottom: var(--bottom-xsmall) ;
    }

    .header__image {
        grid-column: 9/ span 1;
    }

    .header__image img {
        width: 50px;
        border-radius: 100px;
    }
</style>