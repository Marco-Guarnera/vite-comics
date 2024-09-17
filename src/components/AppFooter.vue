<script>
export default {
    data: () => ({
        // Struttura dati
        imgsList: [
            {
                src: "facebook.png",
                alt: "Facebook"
            },

            {
                src: "twitter.png",
                alt: "Twitter"
            },

            {
                src: "youtube.png",
                alt: "YouTube"
            },

            {
                src: "pinterest.png",
                alt: "Pinterest"
            },

            {
                src: "periscope.png",
                alt: "Periscope"
            }
        ]
    }),
    methods: {
        getImgSrc(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <!-- Footer -->
    <footer>
        <div class="upper"></div>
        <div class="lower">
            <div class="wrapper flex row">
                <button>Sign-Up Now!</button>
                <div class="flex row">
                    <h3>Follow Us</h3>
                    <ul class="imgs-list flex row">
                        <li class="imgs-list-item" v-for="img in imgsList"><img :src="getImgSrc(img.src)"
                                :alt="img.alt"></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    .upper {
        height: 375px;
        background-image: url(../assets/img/footer-background.jpg);
        background-size: cover;
    }

    .lower {
        height: 125px;
        background-color: #303030;

        .wrapper {
            height: 100%;
            justify-content: space-between;
            align-items: center;
            padding: 25px;

            button {
                color: #FFF;
                background-color: transparent;
                border: 2px solid #0282F9;
                font-size: 1rem;
                font-weight: bold;
                padding: 15px;
                text-transform: uppercase;
            }

            div {
                align-items: center;
                gap: 25px;

                h3 {
                    color: #0282F9;
                    text-transform: uppercase;
                }

                .imgs-list {
                    gap: 25px;
                }
            }
        }
    }
}
</style>