<template>
  <div>
    <h1>重定向测试页面</h1>

    <button @click="goBack">后退</button>
    <button @click="go">后退两个页面</button>
    <button @click="goHome">回到首页</button>
  </div>
</template>

<script>
export default {
  methods: {
    goBack(){
      this.$router.back()
    },
    go(){
      this.$router.go(-2)
    },
    goHome(){
      // this.$router.push('/')
      // this.$router.push({
      //   path:'/user',
      //   query:{
      //     name:'wangwu',
      //     id:888
      //   }
      // })
      this.$router.push({
        name:'User',
        params:{
          name:'wangwu',
          id:888
        }
      })
    }
  },

};
</script>

<style lang="scss" scoped>

</style>