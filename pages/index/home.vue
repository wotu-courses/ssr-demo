<template>
  <div>
    <ul>
      <li v-for="item in list" :key="item.id">
        {{item.title}} 
        </li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      list: []
    };
  },
  async asyncData() {
    console.log('这里的代码是在服务器运行的');
    try {
      const { data } = await axios.get(
        `http://www.easy-mock.com/mock/5a0561fbe264ca23e8c73023/wotu/live_list`
      );
      return {
        list: data.list
      };
    } catch (err) {
      console.error(err);
    }
  }
};
</script>

<style>

</style>
