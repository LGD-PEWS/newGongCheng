<template>
  <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" :ellipsis="false" @select="handleSelect">
    <img class="logo" src="@/assets/logo.jpg" @click="toHome" />
    <div class="flex-grow" />
    <el-menu-item index="/Products">产品</el-menu-item>
    <el-menu-item index="/News">新闻</el-menu-item>
    <el-menu-item index="/Solutions">解决方案</el-menu-item>
    <el-menu-item index="/Services">咨询与服务</el-menu-item>
    <el-menu-item index="/About">关于信工诚</el-menu-item>
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
            <div class="headerText">专注仿真分析，加速制造创新</div>
          </el-col>
          <el-col :span="1">
          </el-col>
        </el-row>
      </el-header>
      <el-main>
        <RouterView />
      </el-main>
      <el-footer> <el-row class="row-bg" justify="center">
          <div class="weChat">微信公众号:</div>
          &nbsp;&nbsp;&nbsp;&nbsp;
          <img class="QRcode" src="@/assets/QRcode.jpg" />
        </el-row>
        <p>&nbsp;</p>
        <el-row class="row-bg" justify="center">
          <div class="text">版权所有 2009-2021 北京信工诚科技有限公司 京ICP备10217026 京公网安备 11010802036411号</div>
        </el-row>
        <p>&nbsp;</p>
        <el-row class="row-bg" justify="center">
          <div class="text">
            北京市海淀区绿地中央广场林风二路38号院3号楼411室 邮编：100085 电话：010-62640357 传真：010-62646681 电子邮件地址：15699735015@126.com
          </div>
        </el-row>
        <p>&nbsp;</p>
      </el-footer>
    </el-container>
  </div>
</template>

<script setup>
// import { RouterLink, RouterView } from 'vue-router'
import { RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'
import { useRouter } from 'vue-router';

const router = useRouter();

const toHome = () => {
  router.push({ path: '/' })
}

const activeIndex = ref('/')
const handleSelect = (key, keyPath) => {
  console.log(key, keyPath)
  router.push({ path: key })
}
</script>

<style scoped lang="scss">
.flex-grow {
  flex-grow: 1;
}

.header {
  margin-top: 15px;
  line-height: 60px;
}

.headerText {
  text-align: right
}

.logo {
  height: 57.6px;
}

.logo:hover {
  cursor: pointer
}

.weChat {
  font-size: 16px;
  line-height: 70px;
  color: #999
}

.QRcode {
  height: 70px;
}

.text {
  font-size: 12px
}
</style>
