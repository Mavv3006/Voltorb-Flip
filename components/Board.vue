<template>
  <div class="flex justify-center pt-16">
    <div class="block">
      <div class="grid grid-cols-5 grid-rows-5 gap-4">
        <Card
          @click="handleClick(index)"
          :value="entry.value"
          v-for="(entry, index) in data"
          :key="index"
          :is-voltorb="entry.isVoltorb"
        />
      </div>
      <div class="grid grid-cols-5 grid-rows-1 gap-4 mt-4">
        <summary-card
          voltorbCount="20"
          :index="index - 1"
          :value="index"
          v-for="index in 5"
          :key="index"
        />
      </div>
    </div>
    <div class="flex flex-col gap-4 ml-4">
      <summary-card
        voltorbCount="20"
        :index="index - 1"
        :value="index"
        v-for="index in 5"
        :key="index"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  data: {
    isVoltorb: boolean;
    value: number;
  }[];
}>();

const handleClick = (index: number): void => {
  console.debug("clicked", index);
};
</script>

<style></style>
