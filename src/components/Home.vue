<template>
    <section class="home">
        <div class="home__header">
            <Header />
        </div>
        
    </section>
</template>

<script>
import Header from '../components/Header.vue'
	export default {
		components: {
			Header,
		},
	}
</script>

<style>
    .home {
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        column-gap: var(--gap-big)
    }

    .home__header {
        grid-column: 3/ span 10;
    }
</style>