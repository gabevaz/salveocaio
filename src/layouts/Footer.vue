<script setup></script>

<template>
    <!-- Footer Start -->
    <footer class="bg-theme-dark-blue py-10">
        <div class="container mx-auto px-5">
            <div class="md:flex md:justify-between">
                <div class="flex flex-col md:flex-row md:space-x-12 items-baseline">
                    <div class="max-md:mx-auto max-md:mb-8">
                        <a href="/" class="flex items-baseline">
                            <h2 class="font-theme-heading font-medium text-xl text-white">Juntos Pelo Caio</h2>
                            <img src="/images/heart-white.png" alt="logo" class="w-10 ml-3" />
                        </a>
                    </div>
                    <ul
                        class="flex flex-col md:flex-row space-y-5 md:space-y-0 md:space-x-8 text-xs text-center md:text-left font-theme-heading max-md:w-full">
                        <li class="uppercase text-white hover:text-theme-secondary transition duration-200">
                            <a href="#history" v-smooth-scroll>História</a>
                        </li>
                        <li class="uppercase text-white hover:text-theme-secondary transition duration-200">
                            <a href="#hope" v-smooth-scroll>Nossa esperança</a>
                        </li>
                        <li class="uppercase text-white hover:text-theme-secondary transition duration-200">
                            <a href="#features" v-smooth-scroll>O que é CLN7</a>
                        </li>
                        <li class="uppercase text-white hover:text-theme-secondary transition duration-200">
                            <a href="#como-ajudar" v-smooth-scroll>Como ajudar</a>
                        </li>
                        <li class="uppercase text-white hover:text-theme-secondary transition duration-200">
                            <a href="#contact" v-smooth-scroll>Contato</a>
                        </li>
                    </ul>
                </div>
                <div class="md:place-self-end place-self-center mt-10 md:mt-0">
                    <ul class="flex space-x-8 items-center">
                        <li>
                            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"
                                fill="none" stroke="#FFFFFF" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round" class="icon-instagram">
                                <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
                                <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
                                <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
                            </svg>

                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
    <!-- Footer End -->
</template>
