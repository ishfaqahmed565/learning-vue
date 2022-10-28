<script setup>
import ModalItem from "@/components/Teams/ModalItem.vue";
import { ref } from "vue";
import { useTeamStore } from "@/stores/TeamStore.js";
let show = ref(false);
let team = useTeamStore();
</script>

<template>
  <div>
    <button
      class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded disabled:bg-gray-400"
      :disabled="!team.remainingSpots"
      @click="show = true"
    >
      Add Member ({{ team.remainingSpots }} Spots Left)
    </button>
  </div>
  <Teleport to="body">
    <ModalItem :show="show" @close="show = false">
      <template #default> Override the default</template>
    </ModalItem>
  </Teleport>
</template>
