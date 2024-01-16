<template>

  <div class="text-h5 text-primary text-center">
    <q-img class="image" src="src/assets/welcome.jpg" />
  </div>

</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'WelcomePage'
})
</script>

<style lang="scss">
.image{
  position: relative;
  width: 100%;
  height: 100%;
}
</style>
