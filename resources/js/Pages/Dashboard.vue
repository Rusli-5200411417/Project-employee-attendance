<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
import { VContainer, VRow, VApp } from "vuetify/components";
import CardItem from '@/Components/Cards.vue';

const cards = [
  { title: "Users", value: "26K", percentage: "-12.4%", color: "#673AB7", icon: "mdi-account-group" },
  { title: "Income", value: "$6.200", percentage: "40.9% ↑", color: "#2196F3", icon: "mdi-cash" },
  { title: "Conversion Rate", value: "2.49%", percentage: "84.7% ↑", color: "#FFC107", icon: "mdi-chart-line" }
];
</script>

<template>
  <Head title="Dashboard" />

  <AuthenticatedLayout>
    <template #header>
      <h2 class="font-semibold text-xl text-black-800 leading-tight">Dashboard</h2>
    </template>

    <v-app>
      <v-container>
        <v-row>
          <CardItem
            v-for="(card, index) in cards"
            :key="index"
            v-bind="card"
          />
        </v-row>
      </v-container>
    </v-app>

  </AuthenticatedLayout>
</template>
