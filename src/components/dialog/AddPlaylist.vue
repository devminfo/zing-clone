<script lang="ts" setup>
import { ref } from 'vue'

const dialogVisible = ref(true)

const form = reactive({
  name: '',
})
</script>

<template>
  <el-dialog
    v-model="dialogVisible"
    width="330px"
    align-center
    class="dialog-wrapper"
  >
    <template #header>
      <h3 class="text-center text-lg font-bold pl-[14px]!">Tạo playlist mới</h3>
    </template>

    <div class="form-playlist-content">
      <el-form :model="form">
        <el-input v-model="form.name" placeholder="Nhập tên playlist" />
      </el-form>
    </div>

    <template #footer>
      <div class="text-center">
        <el-button round class="w-full" type="primary">Tạo mới</el-button>
      </div>
    </template>
  </el-dialog>
</template>

<style lang="scss">
.dialog-wrapper {
  background-color: var(--primary-bg) !important;

  .el-input__wrapper {
    @apply bg-[var(--alpha-bg)] rounded-full;

    border: 1px solid var(--border-primary);
    outline: none;
    box-shadow: none !important;
    color: var(--text-primary) !important;
  }
}

.form-playlist-content {
  max-width: 290px;
  text-align: center;
}

.el-dialog__headerbtn {
  width: 48px;
  height: 34px;
}

.el-icon.el-dialog__close {
  font-size: 20px;
  color: white !important;
}
</style>
