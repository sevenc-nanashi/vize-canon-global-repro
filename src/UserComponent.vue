<template>
  <!-- Should be type error -->
  <GlobalComponent :thisWantsString="0" />
  <!-- Should not be type error -->
  <GlobalComponent @someEvent="eventHandler" />
  <!-- Should be type error -->
  <QBtn :disable="'string'" />
  <!-- Should not be type error -->
  <QBtn @click="clickHandler" />
</template>
<script setup lang="ts">
function eventHandler(eventArg: string) {
  console.log("Event received from GlobalComponent:", eventArg);
}
function clickHandler(event: Event) {
  console.log("Button clicked!");
}
</script>
