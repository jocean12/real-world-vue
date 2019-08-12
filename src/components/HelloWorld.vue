<template>
  <div>
    <h1>{{ msg }}</h1>
    <!-- <router-link class="spiritual absolute" to="/spiritual"
      >Spiritual</router-link
    >
    <router-link class="mental absolute" to="/mental">Mental</router-link>-->
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #adadad;
}
.spiritual {
  top: 220px;
  left: 420px;
  transform: rotate(-50deg);
}
.mental {
  top: 225px;
  right: 430px;
  transform: rotate(50deg);
}
</style>
