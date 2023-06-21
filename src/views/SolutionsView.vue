<!-- 解决方案 -->
<template>
  <el-row :gutter="20">
    <el-col :span="1">
    </el-col>
    <el-col :span="6">
      <el-card class="box-card-left">
        <template #header>
          <div class="card-header">
            <span>新闻</span>
            <el-button class="button" text>
              <el-icon>
                <DArrowRight />
              </el-icon>
            </el-button>
          </div>
        </template>
        <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>
      </el-card>
      <el-card class="box-card-left2">
        <template #header>
          <div class="card-header">
            <span>咨询</span>
            <el-button class="button" text>
              <el-icon>
                <DArrowRight />
              </el-icon>
            </el-button>
          </div>
        </template>
        <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>
      </el-card>
    </el-col>
    <el-col :span="16">
      <!-- <el-card class="box-card-main">
        <template #header>
          <div class="card-header">
            <span>产品</span>
            <el-button class="button" text>
              <el-icon>
                <DArrowRight />
              </el-icon>
            </el-button>
          </div>
        </template>
        <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>
      </el-card> -->
    </el-col>
    <!-- <el-col :span="6">
      <el-card class="box-card-right">
        <template #header>
          <div class="card-header">
            <span>解决方案</span>
            <el-button class="button" text>
              <el-icon>
                <DArrowRight />
              </el-icon>
            </el-button>
          </div>
        </template>
        <div v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</div>
      </el-card>
    </el-col> -->
    <el-col :span="1">
    </el-col>
  </el-row>
</template>

<script lang="ts" setup></script>

<style scoped lang="scss">
.el-row {
  margin-bottom: 20px;
}

.el-row:last-child {
  margin-bottom: 0;
}

.el-col {
  border-radius: 4px;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

/*  */
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.text {
  font-size: 14px;
}

.item {
  margin-bottom: 18px;
}

.box-card-left {
  // width: 20em;
  // height: 40em;
  margin: auto;
}

.box-card-left2 {
  // width: 20em;
  margin: auto;
  margin-top: 50px;
}

// .box-card-main {
//   width: 30em;
//   height: 25em;
//   margin: auto;
// }


// .box-card-right {
//   width: 20em;
//   height: 40em;
//   margin: auto;
// }
</style>
