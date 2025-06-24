<script setup lang="ts">
import { computed } from "vue";

interface Props {
    label?: string;
    modelValue?: string;
}

const props = defineProps<Props>();

const emit = defineEmits(["update:modelValue"]);

const _modelValue = computed({
  get() {
    return props.modelValue || "";
  },
  set(value: string) {
    emit("update:modelValue", value);
  },
});
</script>
<template>
  <label class="block mb-3">
    <span v-if="label" class="after:content-['*'] after:text-red-500 block text-2xl text-neutral-800 dark:text-neutral-50">{{ label }}</span>
    <input
      v-model="_modelValue"
      placeholder="Nathan.R"
      type="text"
      required="true"
      class="placeholder:text-sm placeholder:italic block w-full p-3 border border-gray-400 rounded-lg focus:outline-lime-600 disabled:opacity-50 invalid:border-red-600"
    />
  </label>
</template>