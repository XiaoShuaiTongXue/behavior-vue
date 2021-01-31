<template>
  <div class="login">
    <div class="logo_login" style="-webkit-app-region: drag">
      <div class="center">
        <img id="my-logo" src="~@/assets/logo.png" alt="#"/>
      </div>
    </div>
    <div class="login_form">
      <form id="login_form" action="/student/login">
        <fieldset>
          <div class="field">
            <label class="label_field">学号:</label>
            <input type="text" v-model="student.studentNumber" placeholder="请输入12位学号"/>
          </div>
          <div class="field">
            <label class="label_field">密码:</label>
            <input type="password" v-model="student.password" placeholder="请输入密码"/>
          </div>
          <div class="field">
            <label class="label_field hidden">hidden label</label>
            <a class="register" href="" @click="doRegister">用户注册</a>
          </div>
          <div class="btn_group">
            <label class="label_field hidden">hidden label</label>
            <input type="button" class="main_bt" id="exit_btn" @click="exit" value="退出"/>
            <input type="button" class="main_bt" id="login_btn" @click="doLogin" value="登录"/>
          </div>
        </fieldset>
      </form>
    </div>
  </div>
</template>
<script>
import axios from 'axios'

const ipcRenderer = require('electron').ipcRenderer
export default {
  data () {
    return {
      student: {
        studentNumber: '',
        password: ''
      }
    }
  },
  methods: {
    doLogin () {
      alert('执行了')
      axios({
        method: 'post',
        url: '/student/login',
        data: this.student
      }).then(function (response) {
        console.log(response.data)
      }).catch(function (error) {
        alert(error)
      })
    },
    doRegister () {
      ipcRenderer.send('register_open')
    },
    exit () {
      ipcRenderer.send('login-close')
    }
  }
}
</script>
<style>
#my-logo {
  width: 150px;
  height: 80px;
}

@import "../../assets/css/style.css";
@import "../../assets/css/bootstrap.min.css";
@import "../../assets/css/responsive.css";
</style>
