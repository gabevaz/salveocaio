<script setup>

import features from '../data/features.js';
import { ref } from 'vue';

let isOpen = ref(1);

</script>

<template>
    <!-- Features Section Start -->
    <div id="features" class="container mx-auto px-5">
        <section class="py-16">
            <div class="w-4/5 md:w-3/5 mx-auto">
                <h2 class="text-3xl md:text-4xl font-semibold font-theme-heading text-center">O que é a CLN7?</h2>
                <p class="text-center mt-7 font-theme-content text-xl">A CLN7 é uma doença
                    genética ultra rara, degenerativa e progressiva, pertencente ao grupo das lipofuscinoses ceróides
                    neuronais, também conhecidas como Doença de Batten.</p>
            </div>

            <div class="mt-10">
                <ul class="flex flex-col items-center md:flex-row justify-center font-theme-heading">
                    <li v-for="feature in features" :key="feature.id"
                        :class="isOpen === feature.id ? 'md:border-b-4 md:border-theme-secondary' : ''"
                        class="w-full md:w-56 cursor-pointer hover:text-theme-secondary transition duration-200 border-b-2 border-t-2 md:border-t-0 flex justify-center">
                        <a @click.prevent="isOpen = feature.id" href="#"
                            :class="isOpen === feature.id ? ' border-theme-secondary' : ''"
                            class="py-5  md:border-b-0 border-b-4">{{ feature.name }}</a>
                    </li>
                </ul>
            </div>

            <div class="mt-16">
                <!-- Tab Content -->
                <template v-for="feature in features" :key="feature.id">
                    <div v-show="isOpen === feature.id" class="grid gap-8 lg:grid-cols-2">
                        <div class="relative">
                            <img class="z-10 w-full rounded-xl aspect-[4/5] object-cover"
                                :src="feature.details.imageUrl" />
                            <div
                                class="-z-10 bg-theme-primary h-52 w-96 sm:h-80 sm:w-full rounded-r-full absolute -left-56 -bottom-16">
                            </div>
                        </div>
                        <div>
                            <div class="mt-10 md:mt-7 font-theme-content text-xl text-center lg:text-left list-disc [&>ul]:pl-5"
                                v-html="feature.details.description"></div>
                        </div>
                    </div>
                </template>
                <!-- Tab Content -->
            </div>
        </section>
    </div>
    <!-- Features Section End -->
</template>
