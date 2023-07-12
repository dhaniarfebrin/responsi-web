<script setup>
import { onMounted, ref } from "vue"
// Menginisialisasi variabel anim sebagai referensi Vue
let anim = ref();

// Menjalankan kode setelah komponen dipasang (mounted)
onMounted(() => {
    // Menunggu 500ms sebelum menjalankan kode berikutnya
    setTimeout(() => {
        // Menggunakan metode goToAndPlay dari animasi Lottie dengan parameter 150
        // untuk memulai animasi pada frame 150, dengan loop (true)
        console.log(anim.value.goToAndPlay(150, true));
        // Memanggil objek anim.value untuk menjalankan animasi Lottie
        anim.value.play();
    }, 500);
});
</script>

<script>
import { LottieAnimation } from "lottie-web-vue";
import HeroAnimation from "/public/img/hero.json";

export default {
    name: 'HeroSection'
    , components: {
        LottieAnimation
    },
}
</script>

<template>
    <section class="bg-white mt-10">
        <div class="container flex flex-col px-6 py-10 mx-auto space-y-6 lg:h-[32rem] lg:py-16 lg:flex-row lg:items-center">
            <div class="w-full lg:w-1/2">
                <div class="lg:max-w-lg">
                    <h1 class="text-l font-bold tracking-wide text-gray-400 lg:text-xl">
                        Dhaniar Febrin Wahyudi_21.11.4308
                    </h1>
                    <h1 class="text-3xl font-bold tracking-wide text-gray-800 lg:text-5xl">
                        Your IT Consultant
                    </h1>

                    <div class="mt-8 space-y-5">
                        <p class="flex items-center -mx-2 text-gray-700 00">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 mx-2 text-blue-500" fill="none"
                                viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>

                            <span class="mx-2">Clean and Simple Layout</span>
                        </p>

                        <p class="flex items-center -mx-2 text-gray-700">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 mx-2 text-blue-500" fill="none"
                                viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>

                            <span class="mx-2">Expensive</span>
                        </p>

                        <p class="flex items-center -mx-2 text-gray-700">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 mx-2 text-blue-500" fill="none"
                                viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>

                            <span class="mx-2">Easy to Use</span>
                        </p>
                    </div>
                </div>

                <div
                    class="w-full mt-8 bg-transparent border rounded-md lg:max-w-sm -700 focus-within:border-blue-400 focus-within:ring focus-within:ring-blue-300 dark:focus-within:border-blue-400 focus-within:ring-opacity-40">
                    <form class="flex flex-col lg:flex-row">
                        <input type="email" placeholder="Enter your email address"
                            class="flex-1 h-10 px-4 py-2 m-1 text-gray-700 placeholder-gray-400 bg-transparent border-none appearance-none focus:outline-none focus:placeholder-transparent focus:ring-0" />

                        <button type="button"
                            class="h-10 px-4 py-2 m-1 text-white transition-colors duration-200 transform bg-blue-500 rounded-md hover:bg-blue-400 focus:outline-none focus:bg-blue-400">
                            Join Us
                        </button>
                    </form>
                </div>
            </div>

            <div class="flex items-center justify-center w-full h-96 lg:w-1/2">
                <!-- <img class="object-cover w-full h-full mx-auto rounded-md lg:max-w-2xl" src="/img/hero.JPG"
                    alt="glasses photo"> -->
                <LottieAnimation :animation-data="HeroAnimation" :loop="true" :auto-play="true" :speed="1" ref="anim" />

            </div>
        </div>
        <div class="fixed inset-x-0 lg:inset-x-auto bottom-6 lg:right-8 xl:right-10 xl:bottom-8">
            <div class="lg:w-72 px-6 lg:px-0">
                <div class="p-2 bg-blue-600 rounded-lg shadow-lg sm:p-3">
                    <div class="flex flex-wrap items-center justify-between">
                        <a target="_blank" href="https://github.com/dhaniarfebrin" class="flex items-center flex-1 w-0">
                            <span class="flex p-2 bg-blue-800 rounded-lg">
                                <svg class="h-6 w-6 text-white" viewBox="0 0 24 24" fill="none"
                                    xmlns="http://www.w3.org/2000/svg">
                                    <path
                                        d="M5.12954 3.00772C5.48563 2.38457 6.14831 2 6.86603 2H17.134C17.8517 2 18.5144 2.38457 18.8704 3.00772L20.0133 5.00772C20.6612 6.14163 20.0618 7.51107 18.9235 7.89532C18.9276 7.97661 18.9269 8.0591 18.9209 8.14249L18.0638 20.1425C17.989 21.1891 17.1181 22 16.0689 22H7.9311C6.88182 22 6.01094 21.1891 5.93618 20.1425L5.07904 8.14249C5.07308 8.0591 5.07231 7.97661 5.07645 7.89531C3.93813 7.51105 3.33874 6.14162 3.98668 5.00772L5.12954 3.00772ZM7.07396 8L7.28824 11H16.7117L16.926 8H7.07396ZM7.71681 17L7.9311 20H16.0689L16.2831 17H7.71681ZM18.2768 6L17.134 4L6.86603 4L5.72317 6H18.2768Z"
                                        fill="currentColor"></path>
                                </svg>

                            </span>

                            <p class="ml-3 font-medium tracking-wide text-white truncate">
                                By me a coffee
                            </p>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>