<template>
  <div>
    <div class="nav_bar">
      <a href="/" class="my_blog">博客</a>
      <el-input v-model="input" placeholder="请输入内容" class="my_input"></el-input>
      <el-col :span="12" class="my_ul" v-if="input === ''">
        <el-dropdown trigger="click">
        <span class="el-dropdown-link">
          我的<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
          <el-dropdown-menu slot="dropdown" class="my_a">
            <el-dropdown-item><a href="/login">登录</a></el-dropdown-item>
            <el-dropdown-item><a href="/register">注册</a></el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-col>

      <el-col :span="12" class="my_ul" v-else>
        <el-dropdown trigger="click">
        <span class="el-dropdown-link">
          我的<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item >
              <img src="../../assets/logo.png" alt="" class="img">
              <p class="p">用户名</p>
            </el-dropdown-item>
            <el-dropdown-item>修改密码</el-dropdown-item>

          </el-dropdown-menu>
        </el-dropdown>
      </el-col>
    </div>
    <div class="user_input">
      <div class="user_title">用户登录</div>
      <div class="user_class">
        <label for="username">用户名</label>
        <el-input id="username" v-model="username" placeholder="请输入用户名" class="user_name"></el-input>
        <el-input v-model="password" placeholder="请输入密码"></el-input>
      </div>

    </div>
  </div>

</template>

<script>
  export default {
    name: "NavBar",
    data() {
      return {
        input: '',
        username: '',
        password: ''
      }
    },
    methods: {

    }
  }
</script>

<style scoped>
  .nav_bar a {
    text-decoration:none;
    color: #666;
  }
  .nav_bar {
    display: flex;
    top: 0;
    left: 0;
    border-bottom: 1px solid #ccc;
    padding-bottom: 10px;
  }
  .nav_bar .my_blog {
    flex: 2;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav_bar .my_input {
    flex: 5;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav_bar .my_ul {
    flex: 2;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .my_a a{
    text-decoration:none;
    color: black;
  }
  .img {
    width: 40px;
    height: 40px;
    padding: 0 6px;
    border-radius: 25px;
    border: 1px solid #ccc;
  }
  .p {
    text-align: center;
  }
  .user_input {
    width: 50%;
    margin-left: 25%;
    margin-top: 10%;
  }
  .user_title {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-bottom: 20px;
  }
  .user_name {
    padding-bottom: 20px;
  }
</style>
