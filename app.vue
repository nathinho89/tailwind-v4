<script setup lang="ts">
import AppButton from "~/components/AppButton.vue";
import AppInput from "~/components/AppInput.vue";
import MainNav from "~/components/MainNav.vue";
import { useDark } from "@vueuse/core";

const isDark = useDark();
</script>

<template>
    <div class="m-10">
    <label for="isDark" class="flex items-center gap-2">
      <input type="checkbox" v-model="isDark">
      <span>Dark Mode</span>
    </label>
    <MainNav />
    <form action="">
      <AppInput label="Username" />
      <AppButton>Submit</AppButton>
    </form>
  </div>
</template>