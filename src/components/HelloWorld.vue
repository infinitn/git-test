<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      s:'9efb8013e24b34b1f2cb22461c28a6fe',
      a:'http://op.juhe.cn/189/bus/busline?key='+ this.s +'&city=上海&bus=990'
    }
  },
  mounted(){
    this.$ajax.get(this.a).then(function(res){
      console.log(res);
    })
  },
  created(){
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
