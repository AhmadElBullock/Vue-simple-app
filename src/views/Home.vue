<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Hello />
  </div>
</template>

<script>
import Hello from '@/components/Hello.vue'

export default {
  name: 'Home',
  components: {
    Hello
  }
}
</script>
