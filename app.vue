<script setup lang="ts">
import AppButton from "~/components/AppButton.vue";
import AppInput from "~/components/AppInput.vue";
import MainNav from "~/components/MainNav.vue";
</script>

<template>
    <div class="m-10">
    <MainNav />
    <form action="">
      <AppInput label="Username" />
      <AppButton>Submit</AppButton>
    </form>
  </div>
</template>