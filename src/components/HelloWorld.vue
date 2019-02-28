<template>
  <div>
    <input v-model="msg">
    <p>msg:{{msg}}</p>
    <p>computed msg ：{{computedMsg}}</p>
    <button @click="greet">Func</button>
  </div>
</template>
<script lang='ts'>
import Vue from 'vue'
// 为了定义带有装饰风格的组件 
import Component from 'vue-class-component'
@Component  //装饰器
export default class HelloWorld extends Vue{
  msg = 124
  // 计算属性
  get computedMsg (){
    return 'computed'+this.msg
  }
  // 方法
  Func(){
    alert('greeting'+ this.msg)
  }
  mounted(){
    this.Func()
  }
}
// export default {
//   data() {
//     return {
//       msg: "zhihui"
//     };
//   },
//   computed: {
//     computedMsg(newvalue, oldvalue) {
//       return "computed" + this.msg;
//     }
//   },
//   methods: {
//     Func() {
//       alert("greeting" + this.msg);
//     }
//   },
// mounted () {
//   this.Func()
// }
// };
</script>
