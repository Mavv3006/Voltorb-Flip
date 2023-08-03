<template>
  <div class="w-[75px] h-[75px] border border-white border-4" :class="[colorMap[props.index]]">
    <div class="h-1/2 upper-line">
      {{ value }}
    </div>
    <hr />
    <div class="h-1/2 lower-line">
      <Dot class="mr-1"/>
      {{ voltorbCount }}
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  voltorbCount: number;
  value: number;
  index: 1 | 2 | 3 | 4 | 5;
}>();

const colorMap = [
  "bg-red-300",
  "bg-green-300",
  "bg-orange-300",
  "bg-blue-300",
  "bg-fuchsia-300",
];
</script>

<style scoped>
hr {
  border: 1px solid black;
}

.upper-line {
  display: flex;
  justify-content: center;
  align-items: center;
}

.lower-line {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
