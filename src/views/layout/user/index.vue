<template>
  <div class="user">
    <!--  搜索部分-->
    <el-form
      :inline="true"
      :model="searchForm"
      ref="searchFormRef"
      label-width="88px"
      class="demo-form-inline"
    >
      <el-form-item label="用户名称">
        <el-input v-model="searchForm.username" style="width:150px"></el-input>
      </el-form-item>
      <el-form-item label="用户邮箱">
        <el-input v-model="searchForm.email" style="width:150px"></el-input>
      </el-form-item>
      <el-form-item label="角色">
        <el-select v-model="searchForm.role_id" style="width:150px" placeholder="请选择">
          <el-option label="超级管理员" value="1"></el-option>
          <el-option label="管理员" value="2"></el-option>
          <el-option label="老师" value="3"></el-option>
          <el-option label="学生" value="4"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">搜索</el-button>
        <el-button type="default" @click="onSubmit">清除</el-button>
        <el-button type="primary" @click="onSubmit">+新增用户</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>


<script>
export default {
  data() {
    return {
      searchForm: {
        username: "",
        email: "",
        role_id: ""
      },
      page: 1,
      limit: 3
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    }
  }
};
</script>