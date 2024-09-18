<script>
import ComicsList from "./ComicsList.vue";

export default {
    components: {
        ComicsList
    }
}
</script>

<template>
    <!-- Main -->
    <main>
        <div class="wrapper">
            <ComicsList />
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: #1C1C1C;
}
</style>