<template>
  <div class="dashboard-container">
    <el-row :gutter="10">
      <el-col :xs="6" :sm="6" :md="4" :lg="3" :xl="6"><div class="grid-content bg-purple">今天</div></el-col>
      <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="6"><div class="grid-content bg-purple">本周</div></el-col>
      <el-col :xs="6" :sm="6" :md="4" :lg="3" :xl="6"><div class="grid-content bg-purple-light">本月</div></el-col>
      <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="6"><div class="grid-content bg-purple-light">上月</div></el-col>
    </el-row>
    <div class="dashboard-text">name: {{ name }}</div>
  </div>
  
</template>

<style>
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
</style>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
