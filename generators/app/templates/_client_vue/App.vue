<template>
  <div class="app">
    hello {{ username }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '...'
    }
  },
  created() {
    f_Request('/getusername', {})
      .then(data => {
        if (!data) return
        this.username = data.username
      })
  }
}
</script>

<style lang="scss" scoped>
.app {
  
}
</style>


