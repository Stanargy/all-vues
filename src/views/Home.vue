<template>
  <div class="home">
    <rootComponent />
  </div>
</template>

<script>
// @ is an alias to /src
import rootComponent from '@/components/rootComponent.vue'

export default {
  name: 'home',
  components: {
    rootComponent
  }
}
</script>

<style scoped>
.home{
  height: 1400px;
}

</style>
