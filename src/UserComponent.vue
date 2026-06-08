<template>
  <GlobalComponent :thisWantsString="0" />
  <GlobalComponent @someEvent="eventHandler" />
</template>
<script setup lang="ts">
function eventHandler(eventArg: string) {
  console.log("Event received from GlobalComponent:", eventArg);
}
</script>
