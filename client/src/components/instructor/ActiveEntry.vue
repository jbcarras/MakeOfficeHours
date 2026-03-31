<script setup lang="ts">

import QueueControlEntry from "@/components/instructor/QueueControlEntry.vue";

defineProps(["student_name", "ubit", "ta_name", "visit_id"])
defineEmits(["end-visit"])


</script>

<template>

  <QueueControlEntry>
    <template #info>{{ student_name }} ({{ ubit }}) is being helped by {{ ta_name }}</template>
    <template #buttons>
      <button class="danger" @click="$emit('end-visit', visit_id)">End Visit</button>
    </template>
    <template #dropdown-buttons>
      <button class="danger" @click="$emit('end-visit', visit_id)">End Visit</button>
    </template>
  </QueueControlEntry>

</template>

<style scoped>

</style>