<script setup>
import { Search } from '@element-plus/icons-vue'
</script>

<template>
    <el-row justify="space-between">
        <el-col class="left" :span="6">
            <el-button type="primary">上传文件</el-button>
            <el-button type="primary">新建文件夹</el-button>
        </el-col>
        <el-col class="right" :span="7">
            <el-input v-model="search" style="width: 240px" placeholder="输入要搜索的文件名" :prefix-icon="Search" />
            <el-button :icon="Search" circle type="primary" />
            <el-button type="primary">重置</el-button>
        </el-col>
    </el-row>
</template>

<style scoped>
.right {
    .el-input {
        margin-right: 10px;
    }
}
</style>