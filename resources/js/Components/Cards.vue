<script setup>
import { VCard, VRow, VCol, VIcon, VDivider, VSheet } from "vuetify/components";

defineProps({
  title: String,
  value: String,
  percentage: String,
  color: String,
  icon: String,
});
</script>

<template>
  <v-col cols="12" sm="6" lg="4">
    <v-card class="pa-3 elevation-2" :style="{ backgroundColor: color }">
      <div class="d-flex justify-space-between align-center">
        <div>
          <h3 class="text-white font-weight-bold">{{ value }}</h3>
          <span class="text-white">{{ title }}</span>
        </div>
        <v-icon color="white" size="32">{{ icon }}</v-icon>
      </div>
      <v-divider class="my-2" />
      <div class="d-flex align-center justify-space-between">
        <span class="text-white text-caption">{{ percentage }}</span>
        <v-icon color="white">mdi-chart-line</v-icon>
      </div>
    </v-card>
  </v-col>
</template>
