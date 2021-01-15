<template>
  <div>
    <input type="number" v-bind:value="count" disabled id="tablo">
    <div class="bord">
      <Key v-on:click="onClick" id="key" v-for="key in keys" v-bind:key="key" :msg="key"></Key>
    </div>
  </div>
</template>
<script>
import Key from "@/components/Key";
export default {
  name: 'Calculator',
  components: {
    Key
  },
  data() {
    return {
      keys: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9],
      count:0,
    }
  },
  methods:{
    onClick(data){
      this.count = data.key;
    }
  }
}
</script>
<style>
#tablo {
  width: 200px;
}

.bord {
  width: 200px;
  height: 200px;
  background: darkgrey;
  margin: auto;
  display: flex;
  flex-flow: row;
}
#key{
  width: 60px;
  height: 60px;
}
</style>
