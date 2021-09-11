<template>
  <div class="about">
    <h1>current team:{{$route.query.title}}</h1>
    <button @click="increase">count</button>
    <h2>{{$store.state.count}}</h2>
    <p>Last team name clicked:{{$route.query.title}}</p>
    <router-link to="/">戻る</router-link>
  </div>
</template>


<script>
export default {
  props: ['data.name'],

  methods:{
    increase(){
      this.$store.commit('incrementMutation');
    }
  }
}
</script>
