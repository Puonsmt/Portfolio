<template>
    <v-btn
        v-show="isVisible"
        class="back-to-top"
        @click="scrollToTop"
        color="black"
        fab 
        style="background-color: black; color: white; border-radius: 50%; width: 40px; height: 40px;min-width: auto"
    >
        <v-icon>fas fa-arrow-up</v-icon>
    </v-btn>
</template>

<script>
export default {
    data() {
        return {
            isVisible: false,
        };
    },

    mounted () {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll(){
            this.isVisible = window.scrollY > 200;
        },
        scrollToTop(){
            window.scrollTo({
                top: 0,
                behavior: "smooth",
            });
        },
    },
};
</script>

<style>
    .back-to-top {
        position: fixed;
        bottom: 50px;
        right: 50px;
        z-index: 1000;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>