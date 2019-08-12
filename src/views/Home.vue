<template>
  <div class="home">
    <img
      alt="Bodhi Tree leaf"
      src="../assets/leaf-2.svg"
      width="500"
      height="715"
      usemap="#cartographyMain"
    />
    <map name="cartographyMain">
      <area
        shape="poly"
        coords="119, 257, 160, 194, 186, 212, 135, 271"
        @click="$router.push('spiritual')"
        v-on:click="triggerEventSpiritual"
        alt="spritual"
      />
      <area
        shape="poly"
        coords="325, 215, 347, 201, 386, 253, 366, 268"
        @click="$router.push('mental')"
        v-on:click="triggerEventMental"
        alt="mental"
      />
      <area
        shape="poly"
        coords="29, 403, 69, 319, 94, 328, 53, 414"
        @click="$router.push('email')"
        alt="email"
      />
    </map>
    <HelloWorld />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  name: 'home',
  components: {
    HelloWorld
  },
  methods: {
    triggerEventSpiritual: function() {
      localStorage.setItem('layerOne', 'spiritual')
    },
    triggerEventMental: function() {
      localStorage.setItem('layerOne', 'mental')
    }
  }
}
</script>
<style>
#app .home img,
.background {
  max-width: 500px;
  position: relative;
}
.absolute {
  position: absolute;
}
area {
  cursor: pointer;
}
</style>
