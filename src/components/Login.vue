<template>
  <div class="login_container">
    登陆组件
    <div class="login_box">
      <div class="avatar_box div">
        <img src="../assets/logo.png" alt="">
      </div>

      <el-form label-width="0" class="login_form" :model="loginForm" :rules="rules">
        <el-form-item prop="name">
          <el-input v-model="loginForm.name" prefix-icon="el-icon-user-solid"></el-input>
        </el-form-item>
        <el-form-item>
          <el-input v-model="loginForm.password" prefix-icon="el-icon-lock" type="password"></el-input>
        </el-form-item>
         <el-form-item class="btns">
          <el-button type="primary" round>登陸</el-button>
          <el-button type="info" round>重置</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {

  data () {
    return {
      loginForm: {
        name: 'haha',
        password: 2
      },
      rules: {
        name: [
          { required: true, message: '请输入活动名称', trigger: 'blur' },
          { min: 1, max: 3, message: '长度在 3 到 5 个字符', trigger: 'blur' }
        ]
      }
    }
  }
}

</script>

<style lang="less" scoped>
  .login_container{
    background-color: #2b4b6b;
    height: 100%;
  }

  .login_box{
    width: 450px;
    height: 300px;
    background-color: #fff;
    border-radius: 3px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
  }

  .avatar_box{
    padding: 10px;
    border: 1px solid #eee;
    border-radius: 50%;
    width: 130px;
    height: 130px;
    position: absolute;
    background-color: #fff;
    left: 50%;
    transform: translate(-50%,-50%);
    img {
      height: 100%;
      width: 100%;
      border-radius: 50%;
      background-color: #eee;
    }
  }

  .btns{
    display: flex;
    justify-content: flex-end;
  }

  .login_form{
    position: absolute;
    bottom: 0;
    width: 100%;
    padding: 20px;
    box-sizing: border-box;
  }
</style>
