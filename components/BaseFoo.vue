<template>
  <div>
    <h2>Component {{ id }}</h2>

    <button @click="setCookie">Set cookie to {{ id }}</button>
    <button @click="resetCookie">Reset cookie</button>

    <p>{{ `${foo}` }}</p>
  </div>
</template>

<script setup lang="ts">
import { toRefs } from 'vue'
import { useCookie } from '#imports'

const props = defineProps({
  id: {
    type: String,
    required: true,
  },
})

const { id } = toRefs(props)

const foo = useCookie<string | undefined>('foo')

const setCookie = () => (foo.value = id.value)
const resetCookie = () => (foo.value = undefined)
</script>
