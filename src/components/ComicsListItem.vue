<script>
export default {
    props: {
        thumbnail: {
            type: String,
            required: true
        },
        series: {
            type: String,
            required: true
        }
    }
}
</script>

<template>
    <li>
        <img :src="thumbnail" :alt="series">
        <span v-text="series"></span>
    </li>
</template>

<style lang="scss" scoped>
li {
    flex-basis: calc(100% / 6 - 25px);

    img {
        margin-bottom: 12.5px;
    }

    span {
        color: #FFF;
    }
}
</style>