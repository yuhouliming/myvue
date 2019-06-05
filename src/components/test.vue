
<script>
    export default {
      el:'test',
      data () {
        return {
          msg: 'Welcome to Your Vue.js App',
          seen:true,
          url:'www.baidu.com',
          input:"",
          message:'wlm'
        }
      },
      methods:{
        reverseMessage:function () {
            this.message=this.message.split('').reverse().join('')
        }
      }
    }
</script>


<template>
  <div>
    <p>{{msg}}</p>
    <div v-html="msg"></div>
    <p v-if="seen">我看到你了</p>
    <div v-if="seen">
        if话语
    </div>
    <div id="test">
      <pre><a v-bind:href="url">百度</a></pre>
    </div>
    <!--->
    <input v-model="input"/>
    <p>{{input}}</p>

    <Button v-on:click = "reverseMessage" type="primary">字符串反转</Button>
    <p>{{message}}</p>

  </div>
</template>

