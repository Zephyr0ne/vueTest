<template>

<div>
<input type="text" v-model="food" @keyup.enter="add" placeholder="请输入菜名"><br>
  今日菜谱： <ul>
    <div v-for="(item,index) in foodList" :key="index">{{item}}</div>
  </ul>
</div>

</template>

<script>
export default {
  data(){
    return{
      foodList:[],
      food:''
    }
  },
  methods:{
    add(){
      this.foodList.push(this.food)
      this.food = ''
    }
  },
  name: "Apex"
}
</script>

<style scoped>

</style>