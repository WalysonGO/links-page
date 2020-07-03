<template>
  <v-card class="ml-4 mr-4 mb-4 elevation-1">
    <v-card-text class="d-flex">
      <img :src="item.image" :alt="item.title" width="48" height="48" />
      <span class="ml-5">
        <div class="font-weight-medium">{{ item.title }}</div>
        <div>
          <a :href="item.url">{{ item.text }}</a>
        </div>
      </span>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    item: { type: Object, required: true },
  },
}
</script>
