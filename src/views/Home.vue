<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">

    <ButtonCounter />
    <ButtonCounter />
    <ButtonCounter />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import ButtonCounter from '@/components/ButtonCounter.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    ButtonCounter
  }
};
</script>
