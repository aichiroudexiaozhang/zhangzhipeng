<template>
  <div class="box">
    <div class="login-img">
      <img src="./logo_index.png" alt="">
    </div>
  <div class="login-werp">
<el-form ref="form" :model="form" label-width="80px">
  <el-form-item>
    <el-input v-model="form.mobile" placeholder="手机号"></el-input>
  </el-form-item>
   <el-form-item>
     <el-col :span="10"> 
    <el-input v-model="form.code "  placeholder="验证码"></el-input>       
     </el-col>
     <el-col :span="10" :offset="2"> 
     <el-button round>发送验证码</el-button>       
     </el-col>
  </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="onSubmit">登陆</el-button>
  </el-form-item>
</el-form>
  </div>
  </div>
</template>
<script>
export default {
  name: 'AppLogin',
  data () {
    return {
    form: {
        mobile: '',
        code: '',
        }
    }
  },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
}
</script>

<style lang='less'>
  .box{
    margin: 200px auto;
    width: 400px;
    text-align: center;
    padding: 20px;
    background-color: aqua;
  }

</style>
