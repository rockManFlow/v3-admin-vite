<script lang="ts" setup>
import { useGreyAndColorWeakness } from "@@/composables/useGreyAndColorWeakness"
import { usePany } from "@@/composables/usePany"
import { useTheme } from "@@/composables/useTheme"
// import { zhCn } from "element-plus/es/locale" // Element Plus 中文包

const { initTheme } = useTheme()
// 这种方式接收暴露的函数功能
const { initGreyAndColorWeakness } = useGreyAndColorWeakness()
// 不要弹窗
// const { initStarNotification, initStoreNotification, initMobileNotification } = usePany()

// 初始化主题
initTheme()

// 初始化灰色模式和色弱模式
initGreyAndColorWeakness()

// #region 初始化通知--定时弹出弹窗的功能
// initStarNotification()

// initStoreNotification()

// initMobileNotification()
// #endregion
</script>

<template>
  <el-config-provider>
    <router-view />
  </el-config-provider>
</template>
