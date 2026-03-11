<script setup lang="ts">

import TableEntry from "@/components/TableEntry.vue";

const props = defineProps(["headings", "table_data"]);

</script>

<template>
  <div id="enrollment-container">
        <table id="enrollment-table">
          <thead>
            <tr>
              <th v-for="heading in headings">{{ heading }}</th>
            </tr>
          </thead>
          <tbody>
            <TableEntry v-for="data in table_data"
                              :data="data">
              <slot></slot>
            </TableEntry>
          </tbody>
        </table>
      </div>
</template>

<style scoped>

th {
  padding: 8px;
}

#enrollment-container {
  justify-content: center;
  overflow-x: scroll;
}

#enrollment-table, tr, th, td {
  border: 2px solid #D9D9D9;
  border-collapse: collapse;
}

#enrollment-table {
  width: 100%;
  font-size: 1rem;
}

#actions {
    display: flex;
    gap: 4px;
    margin: 4px;
    justify-content: center;
}


</style>