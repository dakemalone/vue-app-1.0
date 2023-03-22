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
    <div class="el-dialog-div"></div>
    <!-- :before-close="handleClose" -->
      <span>This is a message</span>
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
.el-dialog-div {
  height: 40vh;
  overflow: auto;
}
</style>
