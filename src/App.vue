<template>
  <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" :ellipsis="false" @select="handleSelect">
    <img class="logo" src="@/assets/logo.jpg" />
    <div class="flex-grow" />
    <el-menu-item index="1">产品</el-menu-item>
    <el-menu-item index="2">新闻</el-menu-item>
    <el-menu-item index="3">解决方案</el-menu-item>
    <el-menu-item index="4">咨询与服务</el-menu-item>
    <el-menu-item index="5">关于信工诚</el-menu-item>
  </el-menu>
  <div class="common-layout">
    <el-container>
      <el-header class="header">
        <el-row class="row-bg" justify="space-evenly">
          <el-col :span="1">
          </el-col>
          <el-col :span="5">
            <el-icon>
              <PhoneFilled />
            </el-icon>
            010-62640357
          </el-col>
          <el-col :span="10">
          </el-col>
          <el-col :span="5">
            <div class="text">专注仿真分析，加速制造创新</div>
          </el-col>
          <el-col :span="1">
          </el-col>
        </el-row>
      </el-header>
      <el-main>
        <RouterView />
      </el-main>
      <el-footer> <el-row class="row-bg" justify="center">
          微信公众号<img class="QRcode" src="@/assets/QRcode.jpg" />
        </el-row>
        <el-row class="row-bg" justify="center">
          版权所有 2009-2021 北京信工诚科技有限公司 京ICP备10217026 京公网安备 11010802036411号
        </el-row>
        <el-row class="row-bg" justify="center">
          北京市海淀区绿地中央广场林风二路38号院3号楼411室 邮编：100085 电话：010-62640357 传真：010-62646681 电子邮件地址：15699735015@126.com
        </el-row>
      </el-footer>
    </el-container>
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'

const activeIndex = ref('1')
const handleSelect = (key, keyPath) => {
  console.log(key, keyPath)
}
</script>

<style>
.flex-grow {
  flex-grow: 1;
}

.header {
  margin-top: 15px;
  line-height: 60px;

  .text {
    text-align: right
  }
}

.logo {
  height: 57.6px;
}

.QRcode {
  height: 4em;
}
</style>
