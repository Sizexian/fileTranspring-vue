<script setup>
import FileBrowser from '@/components/FileBrowser.vue'
import Header from '@/components/Header.vue'
</script>

<template>
    <div>
        <el-container>
            <el-header>
                <Header />
            </el-header>
            <el-main>
                <FileBrowser />
            </el-main>
            <el-footer>
                <el-affix position="bottom" :offset = "10">
                    <el-text>fileTranspring © 2024 </el-text>
                    <el-link href="https://github.com/Sizexian/fileTranspring" target="_blank" type="primary">Github
                        repo</el-link>
                </el-affix>
            </el-footer>
        </el-container>
    </div>
</template>

<style scoped>
</style>
