<template>
  <div class="email">
    Email address
    <input v-model="emailAddress" />
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      emailAddress: ''
    }
  },
  mounted() {
    if (localStorage.emailAddress) {
      this.emailAddress = localStorage.emailAddress
    }
  },
  watch: {
    emailAddress(newEmailAddress) {
      localStorage.emailAddress = newEmailAddress
    }
  }
}
</script>
