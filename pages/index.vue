<template>
  <div>
    <h1>Bug with useCookie</h1>

    <base-foo id="1" key="1" />

    <base-foo id="2" key="2" />
  </div>
</template>

<script lang="ts">
import { defineNuxtComponent } from '#imports'
import BaseFoo from '~/components/BaseFoo.vue'

export default defineNuxtComponent({
  name: 'PageCookies',

  components: {
    BaseFoo,
  },
})
</script>
