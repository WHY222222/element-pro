<template lang="html">
  <div class="login-wrap">
    <div class="login-title">后台管理系统</div>
    <div class="login-form">
      <el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
        <el-form-item label="用户名" prop="username">
          <el-input type="username" placeholder="username" v-model="ruleForm.username"></el-input>
        </el-form-item>
        <el-form-item label="密码" prop="password">
          <el-input type="password" v-model="ruleForm.password"></el-input>
        </el-form-item>

        <el-form-item class="login-btn">
          <el-button type="primary" @click="submitForm('ruleForm')">登录</el-button>
          <el-button >注册</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
  data: function(){
    return{
      ruleForm:{
        username: '',
        password: ''
      },
      rules:{
        username: [
          {required: true, message: '请输入用户名',trigger: 'blur'}
        ],
        password: [
          {required:true, message: '请输入密码',trigger: 'blur'}
        ]
      }
    }
  },
  methods: {
    submitForm(formName){
      const self = this;
      self.$refs[formName].validate((valid) => {
        if(valid){
          localStorage.setItem('ms_username',self.ruleForm.username);
          self.$router.push('/readme');
        } else{
          console.log('error submit!!');
          return false;
        }
      })
    }
  }
}
</script>

<style lang="css" scoped>
</style>
