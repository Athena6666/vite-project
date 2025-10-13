<script lang="ts" setup>
import { ref, reactive } from 'vue'

const form = reactive({
  userName: '',
  passWord: ''
})

const onSubmit = () => {

}

</script>


<template>
  <div class="login">
    <el-card class="card">
      <h2 class="top">登录</h2>
      <el-form :model="form" label-width="80px" size="large">
        <el-form-item prop="userName" label="用户名">
          <el-input v-model="form.userName" style="width: 350px;"></el-input>
        </el-form-item>
        <el-form-item prop="passWord" label="密码">
          <el-input v-model="form.passWord" type="password" style="width: 350px;"></el-input>
        </el-form-item>
      </el-form>
      <div class="bottom">
        <el-button class="button" type="primary" @click="onSubmit()">登录</el-button>
      </div>
    </el-card>
  </div>
</template>


<style lang="scss" scoped>
.login {
  display: flex;
  justify-content: center; //水平居中
  align-items: center; //垂直居中
  height: 100vh;
}

.card {
  width: 500px;
  padding: 20px;
}

.top {
  text-align: center;
  padding-bottom: 20px;
}

.bottom {
  padding-top: 20px;
  text-align: center;
}

.button {
  width: 400px;
  height: 30px;
  font-size: 16px;
  padding: 20px;
}
</style>