<template>
    <section class="home">
        <aside class="home__sidebar">
            <Sidebar />
        </aside>

        <header class="home__header">
            <Header />
        </header>
        
    </section>
</template>

<script>
import Header from '../components/Header.vue';
import Sidebar from '../components/Sidebar.vue';
	export default {
		components: {
			Header,
            Sidebar,
		},
	}
</script>

<style>
    .home {
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        column-gap: var(--gap-big)
    }

    .home__sidebar {
        grid-column: 1/ span 2;
    }

    .home__header {
        grid-column: 3/ span 10;
    }
</style>