<template>
  <q-layout view="lHh Lpr lFf">

    <MainHeader />

    <q-page-container>
      <div class="container">
        <router-view />
      </div>
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import MainHeader from "components/layout/MainHeader.vue";
</script>
