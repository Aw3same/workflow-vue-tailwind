<template>
  <h2 class="!mt-0">{{ props.msg }}</h2>
  <button class="inline-flex items-center px-3 py-2 text-sm font-medium leading-4 text-white bg-red-600 border border-transparent rounded-md shadow-sm hover:bg-red-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500 tabular-nums" @click="increment">
    count is: {{ count }}
  </button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>

<script setup lang="ts">
// useStore, and computed are automatically imported. See vite.config.ts for details.
const store = useStore()
const count = computed(() => store.count)
const props = defineProps<{
  msg: string
  optionalProp?: number
}>()

function increment() {
  store.increment()
}
</script>
