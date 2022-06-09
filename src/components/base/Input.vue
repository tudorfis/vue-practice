
<template>
  <input :value="current" @input="handleInput" />
  <input :value="second" @input="handleInputSecond" />
</template>

<script setup>
const props = defineProps({
  current: [String, Number],
  second: [String, Number],
})

const emit = defineEmits(["update:current", "update:second"]);

function handleInput(event) {
  emit("update:current", event.target.value);
}

function handleInputSecond(event) {
  emit("update:second", event.target.value);
}
</script>