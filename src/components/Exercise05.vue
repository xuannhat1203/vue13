<template>
    <div>
      <v-alert
        v-model="alert"
        border="start"
        close-label="Close Alert"
        color="deep-purple-accent-4"
        title="Xác nhận"
        variant="tonal"
        closable
      >
        Bạn có chắc chắn xóa thông báo này ?
      </v-alert>
  
      <div
        v-if="!alert"
        class="text-center"
      >
        <v-btn @click="alert = true">
          Reset
        </v-btn>
      </div>
    </div>
  </template>

<script>
  export default {
    data: () => ({
      alert: true,
    }),
  }
</script>

<style>

</style>