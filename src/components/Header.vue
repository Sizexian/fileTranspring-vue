<script setup>
import { Search } from '@element-plus/icons-vue'
import { ref } from 'vue';
const centerDialogVisible = ref(false);
const searchCriteria = ref('');
</script>

<template>
    <el-affix :offset = "10">
        <el-row justify="space-between">
            <el-col class="left" :span="6">
                <el-button type="primary" @click="centerDialogVisible = true;">上传文件</el-button>
                <el-button type="primary">新建文件夹</el-button>
            </el-col>
            <el-col class="right" :span="7">
                <el-input v-model="searchCriteria" style="width: 240px" placeholder="输入要搜索的文件名" :prefix-icon="Search" />
                <el-button :icon="Search" circle type="primary" />
                <el-button type="primary">重置</el-button>
            </el-col>
        </el-row>
    </el-affix>

    <el-dialog v-model="centerDialogVisible" title="Warning" width="500" align-center>
        <span>Open the dialog from the center from the screen</span>
        <template #footer>
            <div class="dialog-footer">
                <el-button @click="centerDialogVisible = false">Cancel</el-button>
                <el-button type="primary" @click="centerDialogVisible = false">
                    Confirm
                </el-button>
            </div>
        </template>
    </el-dialog>
</template>

<style scoped>
.right {
    .el-input {
        margin-right: 10px;
    }
}
</style>