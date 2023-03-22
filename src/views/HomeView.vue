<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
    <el-button type="primary" @click="showPlanInfo()">生产计划</el-button>
    <!-- dialog start -->
    <el-button text type="success" @click="dialogVisible = true">
     click to open the Dialog
    </el-button>

    <el-dialog
      v-model="dialogVisible"
      title="Tips"
      width="60%"
    >
    <div class="el-dialog-div">
      <el-text class="mx-1" type="primary">工单: {{ order }}</el-text>
      &nbsp;&nbsp;<el-text class="mx-1" type="success">产品型号: {{ productType }}</el-text>
      <br/>
      <div class="el-progress-div">
        <el-progress type="circle" :percentage="10" status="warning">锡膏！！</el-progress>
        <el-progress type="circle" :percentage="50" status="warning">钢网！！</el-progress>
        <el-progress type="circle" :percentage="70" status="warning">原件！！</el-progress>
        <el-progress type="circle" :percentage="100" status="warning">治具！！</el-progress>
      </div>
    </div>
    <!-- :before-close="handleClose" -->
      <template #footer>
        <span class="dialog-footer">
          <el-button @click="dialogVisible = false">Cancel</el-button>
          <el-button type="primary" @click="dialogVisible = false">
            Confirm
          </el-button>
        </span>
      </template>
    </el-dialog>
    <!-- dialog end -->
    <h1>hello dake</h1>
    <span>{{ count.toFixed(2) }}</span>
    <h2>{{ a }}</h2>
  </div>
</template>

<script lang="ts">
import { ref , defineComponent } from 'vue';
import { ElMessageBox } from 'element-plus'
// import { Options, Vue } from 'vue-class-component';
// import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

// @Options({
//   components: {
//     HelloWorld,
//   },
// })

// export default class HomeView extends Vue {}
export default defineComponent({
  data() {
    return {
      count: 1
    }
  },
  setup(props) {
    console.log(props)
    const order = 80003380;
    const productType = 'PCA-VLWH010-P_1';
    const dialogVisible = ref(false);
    const handleClose = (done: () => void) => {
      ElMessageBox.confirm('Are you sure to close this dialog?')
        .then(() => {
          done()
        })
        .catch(() => {
          // catch error
        })
    }
    const a = ref(1);
    const showPlanInfo = () => {
      a.value++;
    };
    return {
      a,
      order,
      productType,
      dialogVisible,
      handleClose,
      showPlanInfo,
    }
  }
})
</script>
<style scoped>
.dialog-footer button:first-child {
  margin-right: 10px;
}
.el-progress-div {
  position: relative;
  top: calc(2vw);
}
.el-progress {
  margin: 10px 10px 20px 20px;
}
.el-dialog-div {
  height: 40vh;
  overflow: auto;
}
</style>
