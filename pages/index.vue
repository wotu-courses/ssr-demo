<template>
    <div>
      <div class="main">
        <div>logo</div>
        <ul class="nav">
          <li><nuxt-link to="/home">全部live</nuxt-link></li>
          <li><nuxt-link to="/hot">热门精选</nuxt-link></li>
          <li><nuxt-link to="/course">课程与专题</nuxt-link></li>
          <li><nuxt-link to="/me">我的</nuxt-link></li>
        </ul>
      </div>
      <hr>
      <!-- 放子组件 -->
      <div class="child">
        <nuxt-child/>
      </div>
    </div>
</template>

<script>

export default {
  data () {
    return {}
  },
  created () {
    this.$router.push({path: '/home'})
  }
}
</script>

<style>
.main {
  display: flex;
  justify-content: space-between;
  margin: 20px 0;
}
.nav {
  display: flex;
  justify-content: space-around;
  padding-right: 30px;
}
.nav li {
  list-style: none;
  margin-left: 20px;
}
.child {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  /* background: gray; */
  margin-top: 20px;
}
</style>
