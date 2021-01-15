<template>
  <button v-on:click="click()" id="key" >{{msg}}</button>
</template>
<script>
export default {
  name: 'Key',
  props: {
    msg: Number
  },
  data(){
    return {
      key:null,
    }
  },
  methods:{
    click(){
      this.$emit('click', {key:this.key})
      console.log(this.key)
    }
  },
  created() {
    this.key=this.msg;
  }
}
</script>
<style>

</style>
