<template>
  <v-dialog max-width="500">
  <template v-slot:activator="{ props: activatorProps }">
    <v-btn
      v-bind="activatorProps"
      color="surface-variant"
      text="Xác nhận"
      variant="flat"
    ></v-btn>
  </template>

  <template v-slot:default="{ isActive }">
    <v-card title="Dialog">
      <v-card-text>
        Bạn có xác nhận làm mới dữ liệu không ? Nếu có dữ liệu sẽ được câph
      </v-card-text>

      <v-card-actions>
        <v-spacer></v-spacer>

        <v-btn
          text="Xác nhận"
          @click="isActive.value = false"
        ></v-btn>
      </v-card-actions>
    </v-card>
  </template>
</v-dialog>
</template>

<script>
export default {

}
</script>

<style>

</style>