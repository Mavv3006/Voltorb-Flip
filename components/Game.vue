<template>
  <div class="bg-green-500 w-screen h-screen">
    <Board :data="data"/>
    <!-- <button class="mt-8">Neues Spiel</button> -->
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Voltorb Flip Game",
});

const data: {
  isVoltorb: boolean;
  value: number;
}[] = [
    {isVoltorb: true, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
    {isVoltorb: false, value: 3},
];
</script>
