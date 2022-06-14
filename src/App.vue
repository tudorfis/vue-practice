
<template>
  <InnerOutterWrapped 
    :is-wrapped="false"
  />
</template>

<script>
import InnerOutterWrapped from './components/InnerOutterWrapped.vue'

export default {
  name: 'App',
  components: {
    InnerOutterWrapped
  },
}
</script>