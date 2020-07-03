<template>
  <div class="d-flex flex-column mt-7">
    <v-avatar class="mx-auto" size="100">
      <img :src="data.avatar" :alt="data.name" />
    </v-avatar>
    <div class="text-center mt-5 display-1">{{ data.name }}</div>
    <div class="text-center mt-1">{{ data.bio }}</div>
    <div class="mt-10">
      <template v-for="link in data.links">
        <Link :key="link.url" :item="link" />
      </template>
    </div>
  </div>
</template>

<script>
import config from '../config.json'

export default {
  data: () => ({
    data: config,
  }),
}
</script>
