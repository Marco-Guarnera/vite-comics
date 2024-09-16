<script>
export default {
    data: () => ({
        // Struttura dati
        list: ["Characters", "Comics", "Movies", "TV", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"]
    })
}
</script>

<template>
    <!-- Header -->
    <header class="wrapper flex row">
        <img src="../assets/img/logo.png" alt="DC">
        <nav>
            <ul class="flex row">
                <li v-for="item in list"><a href="#" v-text="item"></a></li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
header {
    min-height: 125px;
    justify-content: space-between;
    align-items: center;
    padding: 25px;

    img {
        height: 75px;
    }

    ul {
        gap: 25px;

        li {
            font-size: 0.875rem;
            font-weight: bold;
            text-transform: uppercase;

            a {
                color: #000;

                &:hover {
                    color: #0282F9;
                }
            }
        }
    }
}
</style>