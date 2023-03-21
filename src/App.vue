<template>
  <headerCom></headerCom>
  <router-view />
</template>
<script lang="ts">
import headerCom from '@/components/headerCom.vue'
export default {
  name: 'app',
  components: {
    headerCom
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
ul {
  list-style: none;
  padding-left: 80%;
  li {
    float: left;
    margin-left: 20px;
  }
}
</style>
