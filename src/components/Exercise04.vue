<template>
    <div class="text-center">
      <v-btn color="primary">
        Open menu
  
        <v-menu activator="parent">
          <v-list>
            <v-list-item v-for="i in data" :key="i" link>
              <v-list-item-title>{{ i }}</v-list-item-title>
              <template v-slot:append>
                <v-icon icon="mdi-menu-right" size="x-small"></v-icon>
              </template>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-btn>
    </div>
  </template>

<script setup>
    const data = ["Thông tin cá nhân", "Đổi mật khẩu", "Đăng xuất"]
</script>

<style>

</style>