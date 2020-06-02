<template>
<div>
  <input type="text" v-model="msg">
  <div>{{reverseMsg}}</div>
  <div>{{str}}</div>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      str: ''
    }
  },
  methods:{
    doSomething(){
      console.log('do something');
    }
  },
  computed:{
    reverseMsg:function(){
      return this.msg.split('').reverse().join('');
    }
  },
  watch:{
    msg:function(val){
      this.str = val + ' nihao123';
    }
  },
  filters:{
    up:function(word){
      return word.toUpperCase();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
