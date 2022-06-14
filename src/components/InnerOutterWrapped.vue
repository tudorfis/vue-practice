
<template>
  <div 
    ref="innerContent"
    style="border: 3px solid blue; padding: 3rem;"
  >
    <h1>inner content</h1>
  </div>
  <div 
    ref="wrapperContent" 
    v-show="isWrapped"
    style="border: 3px solid red; padding: 3rem;"
  />
</template>

<script>
import { ref, onMounted } from 'vue'

export default {
  name: 'InnerOutterWrapped',
  props: {
    isWrapped: {
      type: Boolean,
      default: true
    }
  },
  setup(props) {
    const innerContent = ref()
    const wrapperContent = ref()

    onMounted(() => {
      if (props.isWrapped) {
        wrapperContent.value.append(innerContent.value)
      }
    })

    return {
      innerContent,
      wrapperContent,
    }
  },
}
</script>