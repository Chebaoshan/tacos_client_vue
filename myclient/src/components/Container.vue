<template>
  <a-layout style="min-height: 100vh;min-width: max-content;">
    <a-layout-sider v-model:collapsed="collapsed" collapsible>
      <div class="logo" />
      <a-menu theme="white" v-model:selectedKeys="selectedKeys" mode="inline">
        <a-menu-item key="1">
          <money-collect-outlined />
          <span>薪资管理</span>
        </a-menu-item>
        <a-menu-item key="2">
          <desktop-outlined />
          <span>项目管理</span>
        </a-menu-item>
        <a-sub-menu key="sub1">
          <template #title>
            <span>
              <user-outlined />
              <span>用户权限</span>
            </span>
          </template>
          <a-menu-item key="3">人事</a-menu-item>
          <a-menu-item key="4">财务</a-menu-item>
          <a-menu-item key="5">营业</a-menu-item>
        </a-sub-menu>
        <a-sub-menu key="sub2">
          <template #title>
            <span>
              <team-outlined />
              <span>部门管理</span>
            </span>
          </template>
          <a-menu-item key="6">开发一课</a-menu-item>
          <a-menu-item key="8">开发二课</a-menu-item>
          <a-menu-item key="8">开发三课</a-menu-item>
          <a-menu-item key="8">开发二课</a-menu-item>
        </a-sub-menu>
        <a-menu-item key="9">
          <file-outlined />
          <span>报表导出</span>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-content style="margin: 0 16px">
        <a-breadcrumb style="margin: 16px 0">
          <a-breadcrumb-item>用户权限</a-breadcrumb-item>
          <a-breadcrumb-item>人事总</a-breadcrumb-item>
        </a-breadcrumb>
        <div :style="{ padding: '24px', background: '#fff', minHeight: '360px' }">
          未实装
        </div>
      </a-layout-content>
      <a-layout-footer style="text-align: center">
        原型开发
      </a-layout-footer>
    </a-layout>
  </a-layout>
</template>
<script setup lang="ts">
import {
  MoneyCollectOutlined,
  DesktopOutlined,
  UserOutlined,
  TeamOutlined,
  FileOutlined,
} from '@ant-design/icons-vue';
import { ref, reactive, toRefs } from "vue";
const data =reactive({
    collapsed: ref<boolean>(false),
    selectedKeys: ref<string[]>(['1'])
})
const dataAsRefs = toRefs(data)
const { collapsed, selectedKeys} = dataAsRefs
</script>
<style scoped>
#components-layout-demo-side .logo {
  height: 32rem;
  margin: 16rem;
  background: white;
}

.site-layout .site-layout-background {
  background: white;
}
[data-theme='dark'] .site-layout .site-layout-background {
  background: whitesmoke;
}
</style>
