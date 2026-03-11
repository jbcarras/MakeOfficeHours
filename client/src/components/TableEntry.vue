<script setup lang="ts">

const props = defineProps(['data'])

</script>

<template>
          <tr>
            <td v-for="entry in data">{{ entry }}</td>
            <slot/>
          </tr>
</template>

<style scoped>


  tr, th, td {
    border: 2px solid #D9D9D9;
    border-collapse: collapse;
  }

  td {
    padding: 8px;
  }

  tr:nth-child(odd) {
    background-color: #FAFAFA;
  }


</style>