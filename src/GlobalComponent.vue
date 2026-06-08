<template>
  <div>
    <h1>Global Component</h1>
    <p>
      This is a global component that can be used anywhere in the application.
    </p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  thisWantsString?: string;
}>();

defineEmits<{
  someEvent: [eventArg: string];
}>();
// This component is registered globally in main.ts, so it can be used in any other component without needing to import it.
</script>
