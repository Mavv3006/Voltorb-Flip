<template>
  <div
    class="w-[75px] h-[75px] text-white text-center align-middle border border-white border-4"
    @click="handleClick()"
    :class="[isClicked ? 'bg-[#BB8A83]' : 'bg-[#008661]']"
  >
    <div v-if="isClicked">
      <div v-if="isVoltorb">
        <Dot />
      </div>
      <div v-else>
        {{ value }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  value: number;
  isVoltorb: boolean;
}>();

const isClicked = ref(false);

const emit = defineEmits(["click"]);

const handleClick = () => {
  isClicked.value = true;
  emit("click");
};
</script>

<style scoped>
div {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
