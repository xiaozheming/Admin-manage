<template>
  <div class="container">
    <div class="form-container">
      <img src="@/assets/img/login/form-background.png" />
      <div>
        <el-form :model="form" label-width="120px">
          <el-form-item label="用户名">
            <el-input v-model="form.name" />
          </el-form-item>
          <el-form-item label="密码">
            <el-input v-model="form.password" />
          </el-form-item>
        </el-form>
        <el-button type="primary">登录</el-button>
      </div>
    </div>
  </div>
</template>
<script>
import '@/assets/js/canvas-nest.min.js'
export default {
  data() {
    return {
      form: {
        name: '',
        password: ''
      }
    }
  },
  mounted() {
    this.$nextTick(() => {
      document.getElementsByTagName('canvas')[0].className = 'index_bg'
    })
  }
}
</script>

<style lang="less" scoped>
.container {
  width: 100%;
  height: 100%;
  display: flex;
  background-image: url('@/assets/img/login/background.jpg');
}

.form-container {
  width: 670px;
  height: 350px;
  margin: auto;
  display: flex;
  background-color: white;
  z-index: 1;

  img {
    width: 286px;
  }
}

//登录页动画
.index_bg {
  width: 100%;
  height: 100vh;
  background: rgba(0, 0, 0, 0.6) !important;
  z-index: 0 !important;
}
</style>
