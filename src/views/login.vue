<template>
  <div id="layout">
    <div class="layout-login">
      <div class="layout-login-form">
        <el-form
          :model="ruleForm"
          status-icon
          :rules="rules"
          ref="ruleForm"
          label-width="100px"
          class="demo-ruleForm"
        >
          <el-form-item label="账号" prop="account">
            <el-input v-model="ruleForm.account" autocomplete="off"></el-input>
          </el-form-item>

          <el-form-item label="密码" prop="password">
            <el-input type="password" v-model="ruleForm.password" autocomplete="off"></el-input>
          </el-form-item>

          <el-form-item>
            <el-button type="primary" @click="submitForm('ruleForm')">提交</el-button>
            <el-button @click="resetForm('ruleForm')">重置</el-button>
          </el-form-item>
        </el-form>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Login",
  data() {
    var validatePassword = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请输入密码"));
      } else {
        callback();
      }
    };
    var validateAccount = (rule, value, callback) => {
      if (value === "") {
        callback(new Error("请输入账号"));
      } else {
        callback();
      }
    };

    return {
      ruleForm: {
        password: "",
        account: ""
      },
      rules: {
        password: [{ validator: validatePassword, trigger: "blur" }],
        account: [{ validator: validateAccount, trigger: "blur" }]
      }
    };
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert("submit!");
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
    resetForm(formName) {
      this.$refs[formName].resetFields();
    }
  }
};
</script>


<style scoped>
#layout {
  width: 100%;
  height: 100%;
  /* background: red; */
  display: flex;
  align-items: center;
  justify-content: center;
}

#layout .layout-login {
  width: 400px;
  height: 300px;
  /* background:grey; */

  border: 2px;
  border-radius: 4px;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);

  display: flex;
  align-items: center;
  justify-content: center;
}

.layout-login-form {
  width: 70%;

  padding-left: -10px;
}

#layout .boder {
  /* background: red; */

  padding-bottom: 48px;
  width: 300px;
  height: 300px;
  border: 2px;
  border-radius: 4px;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);

  display: block;
}
</style>