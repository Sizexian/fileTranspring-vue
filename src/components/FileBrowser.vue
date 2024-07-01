<script setup>
import { Edit, Delete, Download } from '@element-plus/icons-vue'

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
    <el-table :data="tableData" style="width: 100%;">
        <el-table-column prop="fileName" label="文件名" />
        <el-table-column prop="fileSize" label="文件大小" />
        <el-table-column prop="creationDate" label="创建日期" />
        <el-table-column prop="modifiedDate" label="修改日期" />
        <el-table-column label="操作">
            <template #default="{ row }">
                <el-button type="success" :icon="Download" circle />
                <el-button :icon="Edit" circle plain type="primary" @click=""></el-button>
                <el-button :icon="Delete" circle plain type="danger" @click=""></el-button>
            </template>
        </el-table-column>
    </el-table>
</template>

<style scoped></style>