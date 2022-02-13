<template>
    <aside class="sidebar">
       <ul>
            <li>
                <a href="">
                    <img src="/images/svg/logo.svg" alt="">
                </a>

                <a href=""  v-for="link in links" :key="link" class="sidebar__links">
                    <img :src="link.file" :alt="link.caption">

                    <p>{{ link.title }}</p>

                </a>
            </li>
       </ul>
    </aside>
</template>

<script>
    export default {
        data() {
            return {
                links: [ 
                    { 
                        title: 'Home',
                        file: '/images/svg/home.svg',
                        caption: 'home-logo'

                    },

                    { 
                        title: 'Inbox',
                        file: '/images/svg/inbox.svg',
                        caption: 'inbox-logo'

                    },

                    { 
                        title: 'Notifications',
                        file: '/images/svg/notifications.svg',
                        caption: 'notifications-logo'

                    },

                    { 
                        title: 'My Team',
                        file: '/images/svg/team.svg',
                        caption: 'team-logo'

                    },

                    { 
                        title: 'Search',
                        file: '/images/svg/search.svg',
                        caption: 'search-logo'

                    },  
                ],
                
            }
            
        },
    }
</script>

<style>
    .sidebar {
        background-color: #292F4C;
        height: 100vh;
    }

    .sidebar__links > img {
        width: 30px;
    }

    .sidebar__links {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: var(--bottom-big);
        color: var(--white);
        text-decoration: none;

    }
</style>