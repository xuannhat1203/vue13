<template>
    <v-card>
      <v-toolbar
        color="deep-purple-accent-4"
      >
        <template v-slot:extension>
          <v-tabs
            v-model="currentItem"
            fixed-tabs
          >
            <v-tab
              v-for="item in items"
              :key="item"
              :text="item"
              :value="'tab-' + item"
            ></v-tab>
          </v-tabs>
        </template>
      </v-toolbar>
  
      <v-tabs-window v-model="currentItem">
        <v-tabs-window-item
          v-for="item in items.concat(more)"
          :key="item"
          :value="'tab-' + item"
        >
          <v-card flat>
            <v-card-text>
              <h2>{{ item }}</h2>
              {{ text }}
            </v-card-text>
          </v-card>
        </v-tabs-window-item>
      </v-tabs-window>
    </v-card>
  </template>

<script>
  export default {
    data: () => ({
      currentItem: 'tab-Web',
      items: [
        'Trang chủ', 'Giới thiệu', 'Liên hệ',
      ],
    }),

    methods: {
      addItem (item) {
        const removed = this.items.splice(0, 1)
        this.items.push(
          ...this.more.splice(this.more.indexOf(item), 1),
        )
        this.more.push(...removed)
        this.$nextTick(() => { this.currentItem = 'tab-' + item })
      },
    },
  }
</script>

<style>

</style>