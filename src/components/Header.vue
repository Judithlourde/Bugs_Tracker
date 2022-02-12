<template>
    <section class="header">
        <h1>{{ title }}</h1>
        <p>{{ description }}</p>
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Bugs Tracker',
            description: 'The board for only fun, no offence'
        }
        
    },
}
</script>