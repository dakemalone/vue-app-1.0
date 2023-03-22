<template>
  <div>
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
      @select="handleSelect"
    >
      <el-menu-item index="1">
        <router-link to="/">

          <div>
            <div>
              <el-icon><img src="../assets/icons/网络系统.svg"  /></el-icon>
            </div>
            <span>系统建模</span>
          </div>
        </router-link>
      </el-menu-item>
      <el-menu-item index="2">
        <template #title>
          <router-link to="/"></router-link>
          <div>
            <div>
              <el-icon><img src="../assets/icons/权限.svg"  /></el-icon>
            </div>
            <span>权限管理</span>
          </div>
        </template>
        <!-- <el-menu-item index="2-1">item one</el-menu-item>
      <el-menu-item index="2-2">item two</el-menu-item>
      <el-menu-item index="2-3">item three</el-menu-item>
      <el-sub-menu index="2-4">
        <template #title>item four</template>
        <el-menu-item index="2-4-1">item one</el-menu-item>
        <el-menu-item index="2-4-2">item two</el-menu-item>
        <el-menu-item index="2-4-3">item three</el-menu-item>
      </el-sub-menu> -->
      </el-menu-item>
      <el-menu-item index="3">
        <router-link to="/home">

          <div>
            <div>
              <el-icon><img src="../assets/icons/生产退料.svg"  /></el-icon>
            </div>
            <span>生产管理</span>
          </div>
        </router-link>
      </el-menu-item>
      <el-menu-item index="4">
        <router-link to="/about">

          <div>
            <div>
              <el-icon><img src="../assets/icons/皮革、毛皮、羽毛及其制品和制鞋业.svg"  /></el-icon>
            </div>
            <span>在制品管理</span>
          </div>
        </router-link>
      </el-menu-item>
      <el-menu-item index="5">
        <div>
          <div>
            <el-icon><img src="../assets/icons/物料.svg"  /></el-icon>
          </div>
          <span>物料管理</span>
        </div>
      </el-menu-item>
      <el-menu-item index="5">
        <div>
          <div>
            <el-icon><img src="../assets/icons/设备.svg"  /></el-icon>
          </div>
          <span>治具管理</span>
        </div>
      </el-menu-item>
      <el-menu-item index="6">
        <div>
          <div>
            <el-icon><img src="../assets/icons/工具3.svg"  /></el-icon>
          </div>
          <span>设备管理</span>
        </div>
      </el-menu-item>
      <el-menu-item index="7">
        <div>
          <div>
            <el-icon><img src="../assets/icons/医疗质量分析.svg"  /></el-icon>
          </div>
          <span>质量管理</span>
        </div>
      </el-menu-item>
      <el-menu-item index="8">
        <div>
          <div>
            <el-icon><img src="../assets/icons/包装.svg"  /></el-icon>
          </div>
          <span>包装管理</span>
        </div>
      </el-menu-item>
      <el-menu-item index="9">
        <div>
          <div>
            <el-icon><img src="../assets/icons/查询.svg"  /></el-icon>
          </div>
          <span>系统查询</span>
        </div>
      </el-menu-item>
      <el-menu-item index="10">
        <div>
          <div>
            <el-icon><img src="../assets/icons/personal-center.svg"  /></el-icon>
          </div>
          <span>个人中心</span>
        </div>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
span {
  font-size: calc(1vw);
  display: flex;
  flex-direction: column;
  position: relative;
  margin-top: -25px;
}
a {
  text-decoration: none;
}
img {
  width: calc(2vw);
  height: calc(2vw);
}
/* .router-link-active {
  text-decoration: none;
} */
</style>
