<script>
export default {
    data (){
        return {
            links: [
                {
                    text: 'CHARACTERS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COMICS',
                    url: '#',
                    current: true,
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'GAMES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'FANS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'NEWS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'SHOP',
                    url: '#',
                    current: false,
                },



            ],
        }
    }
};
</script>

<template>
    <header>
        <img class="logo" src="/dc-logo.png" alt="">
        <ul>
            <li v-for="link in links">
                <a :href="link.url" >
                {{ link.text }}
                </a>
            </li>
           
        </ul>
    </header>
</template>

<style lang="scss" scoped>
// @use '../styles/partials/mixins' as *;

header {
// @include center;
display: flex;
justify-content: space-around;
.logo {
    width: 100px;
}

ul{
    margin:0;
    padding: 0;

    li {
        display: inline-block;
        padding: 1rem;

        a:hover {
            color: blue;
            padding-bottom: 3rem;
            border-bottom: 10px solid blue;
        }

        a {
            text-decoration: none;
            color: black;
        }
        
    }
}
}
</style>