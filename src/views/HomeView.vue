<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <p>{{ getNumber }}</p>
    <p @click="getClick()">Click</p>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import {mapGetters, mapActions} from 'vuex'

export default {
  name: 'HomeView',
  computed: mapGetters(['getNumber']),
  methods: mapActions(['getClick']),
  components: {
    HelloWorld
  }
}
</script>
