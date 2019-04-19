<template>
  <div>
    <h2>这是一个Vue2.6路由+Vuex的测试</h2>
    <h3>{{update}}</h3>
    <h3>{{addContent}}</h3>
  </div>
</template>

<script>
  import {mapActions,mapState,mapGetters } from 'vuex'
  export default {
    computed:{
      ...mapState(['update']),
      ...mapGetters(['addContent'])
    },
    mounted(){
      this.setUpdate('hxr')
    },
    watch:{
      update(val){
        console.log(val);
      }
    },
    methods:{
      ...mapActions(['setUpdate']),
    }
  }
</script>

<style scoped>
h2{
  text-align: center;
  font-weight: 700;
}
</style>