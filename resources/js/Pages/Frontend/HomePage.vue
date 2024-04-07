<script setup>
import { Head } from '@inertiajs/vue3';
import GuestLayout from '@/Layouts/GuestLayout.vue';
import HeroComponent from '../../Components/Frontend/Home/HeroComponent.vue';
import AwesomeCarComponent from '../../Components/Frontend/Car/AwesomeCarComponent.vue';
import CounterComponent from '../../Components/Frontend/Home/CounterComponent.vue';

</script>

<template>
    <Head>
        <title>Smart Car Rental System by Shakil Khan</title>
    </Head>

    <GuestLayout>
        <HeroComponent />
        <AwesomeCarComponent />
        <CounterComponent />
    </GuestLayout>
</template>

<style scoped></style>
