<script setup lang="ts">
const item = {
  date: '2016-05-02',
  name: 'Tom',
  address: 'No. 189, Grove St, Los Angeles',
}
const tableData = ref(Array.from({ length: 50 }).fill(item))
</script>
<template>
  <el-container class="h-screen!">
    <!-- sidebar  -->
    <el-aside class="h-screen!">
      <Sidebar />
    </el-aside>

    <!-- main -->
    <el-container class="bg-[var(--layout-bg)]!">
      <el-header class="h-70px! bg-[var(--layout-header-bg)]!">
        <Header />
      </el-header>

      <el-main>
        <slot></slot>
      </el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</template>

<style scoped lang="scss">
.table-dark {
  background-color: var(--layout-bg) !important;
}
</style>
