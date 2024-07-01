<script setup>
import { Search, Edit, Delete, Download } from '@element-plus/icons-vue'

import { ref } from 'vue';
const tableData = ref([
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
    {
        fileName: '文件名',
        fileSize: '5Mb',
        creationDate: '2016-05-03',
        modifiedDate: '2016-05-03',
    },
]);
</script>

<template>
    <el-main>
        <el-card>
            <template #header>
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
            <el-table :data="tableData" style="width: 100%;height: 95%;">
                <el-table-column prop="fileName" label="文件名" />
                <el-table-column prop="fileSize" label="文件大小" />
                <el-table-column prop="creationDate" label="创建日期" />
                <el-table-column prop="modifiedDate" label="修改日期" />
                <el-table-column label="操作">
                    <template #default="{ row }">
                        <el-button type="success" :icon="Download" circle />
                        <el-button :icon="Edit" circle plain type="primary" @click="showDialog(row)"
                            :disabled="isBanned == '1'"></el-button>
                        <el-button :icon="Delete" circle plain type="danger" @click="deleteCategory(row)"
                            :disabled="isBanned == '1'"></el-button>
                    </template>
                </el-table-column>
            </el-table>
        </el-card>
    </el-main>
</template>

<style scoped>
.right {
    .el-input {
        margin-right: 10px;
    }
}
</style>