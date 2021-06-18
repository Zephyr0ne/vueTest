<template>
<div id="test" >
  <button @click="pref" v-if="index>0" > 上一页 </button>
  {{index+1}}
  <button @click="next" v-if="index<9"> 下一页 </button>
</div>
</template>

<script>
export default {
  data(){
    return {
      index: 0,
    }
  },
  methods:{
    pref(){
      this.index--
    },
    next(){
      this.index++
    },
  },
  name: "test"
}
</script>

<style scoped>

</style>