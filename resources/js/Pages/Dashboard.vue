<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-black-800 leading-tight">Dashboard</h2>
        </template>
       <template #default>
            
       </template>
    </AuthenticatedLayout>

</template>




