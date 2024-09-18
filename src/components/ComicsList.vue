<script>
import ComicsListItem from "./ComicsListItem.vue"

export default {
    components: {
        ComicsListItem
    },
    data: () => ({
        comicsList: [
            {
                thumbnail: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                price: "$19.99",
                series: "Action Comics",
                type: "Comic Book"
            },

            {
                thumbnail: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                price: "$3.99",
                series: "American Vampire 1976",
                type: "Comic Book"
            },

            {
                thumbnail: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                price: "$16.99",
                series: "Aquaman",
                type: "Graphic Novel"
            },

            {
                thumbnail: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                price: "$2.99",
                series: "Batgirl",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                price: "$3.99",
                series: "Batman",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                price: "$2.99",
                series: "Batman Beyond",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                price: "$3.99",
                series: "Batman/Superman",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                price: "$4.99",
                series: "Batman/Superman Annual",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                price: "$5.99",
                series: "Batman: The Joker War Zone",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                price: "$6.99",
                series: "Batman: Three Jokers",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                price: "$4.99",
                series: "Batman: White Knight Presents: Harley Quinn",
                type: "Comic Book"
            },

            {
                thumbnail: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                price: "$16.99",
                series: "Catwoman",
                type: "Graphic Novel"
            }
        ]
    })
}
</script>

<template>
    <ul class="flex row">
        <ComicsListItem v-for="comic in comicsList" :thumbnail="comic.thumbnail" :series="comic.series" />
    </ul>
</template>

<style lang="scss" scoped>
ul {
    justify-content: space-between;
    gap: 25px;
    padding: 25px;
}
</style>