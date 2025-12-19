<script setup>
import downloads from "../data/downloads";
import { ref } from 'vue';

let isCopied = ref(false);

function copyEmail() {
    navigator.clipboard.writeText("salveocaio@gmail.com");
    isCopied.value = true;
    setTimeout(() => {
        isCopied.value = false;
    }, 2000);
}
</script>

<template>
    <!-- Download Section Start -->
    <div id="como-ajudar" class="container mx-auto px-5 md:w-4/5">
        <section class="md:py-16">
            <div class="w-4/5 md:w-3/5 mx-auto">
                <h2 class="text-3xl md:text-4xl font-theme-heading font-medium text-center">Como você pode ajudar</h2>
                <p class="text-center text-xl font-theme-content mt-7">Abaixo, você encontrará
                    as formas de doação.
                    <br />Qualquer valor faz diferença. Cada doação nos aproxima do tratamento.
                    <br />E, se não puder doar, compartilhar essa história também salva vidas.
                </p>
            </div>
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8 mt-12">
                <div v-for="(download, index) in downloads" :key="download.id" class="shadow-lg rounded-lg">
                    <div class="flex justify-center mt-12 aspect-square">
                        <img :src="download.icon" alt="Browser Logo" />
                    </div>
                    <h3
                        class="text-2xl font-theme-heading font-medium text-center mt-6 min-h-[64px] px-4 flex items-center justify-center">
                        {{ download.title }}
                    </h3>
                    <div class="my-7">
                        <img class="w-full" src="/images/bg-dots.svg" alt="Dot Backaground" />
                    </div>
                    <div class="flex justify-center mb-8">
                        <button v-if="download.link == 'isEmail'" @click="copyEmail"
                            class="font-theme-heading font-medium bg-theme-primary px-6 py-2 text-white rounded shadow-md hover:bg-white border-2 border-transparent hover:border-theme-primary hover:text-theme-primary cursor-pointer transition duration-200">
                            <span v-if="isCopied">Email copiado</span>
                            <span v-else>{{ download.linkTitle }}</span>
                        </button>
                        <a v-else :href="download.link" target="_blank"
                            class="font-theme-heading font-medium bg-theme-primary px-6 py-2 text-white rounded shadow-md hover:bg-white border-2 border-transparent hover:border-theme-primary hover:text-theme-primary cursor-pointer transition duration-200">
                            {{ download.linkTitle }}
                        </a>
                    </div>
                </div>
            </div>
        </section>
    </div>
    <!-- Download Section End -->
</template>
