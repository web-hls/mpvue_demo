<template>
  <div>
    <!-- <navigation-bar title="携程" background="" color=""></navigation-bar> -->
    
    <div class="banner">
      1
    </div>


    
    <div :class="[isActive ? 'htmlActive' : '', 'errorClass']"> html绑定class </div>
    <div :class="computedClassObject"> js绑定class </div>

    <div :style="{ color : isActive ? 'green' : '' }"> html绑定style </div>
    <div :style="computedStyleObject"> style绑定style </div>

    <van-cell title="姓名" is-link>
        <div>
            <input type="text">
        </div>
    </van-cell>

  </div>
</template>

<script>
import navigationBar from '@/components/navigationBar'

export default {
  components: {navigationBar},
  data () {
    return {
      isActive: true
    }
  },
  computed: {
    computedClassObject() {
      return [ this.isActive ? 'jsActive' : '', 'errorClass' ]
    },
    computedStyleObject() {
      return { color : this.isActive ? 'yellow' : '' }
    }
  }
}

</script>

<style scoped>
.banner {
  height: 300px;
  width: 100%;
  /* position:fixed; */
  /* top:0; */
  background: linear-gradient(to right,#0080FF,#2894FF,#66B3FF)
}
.htmlActive {
  color:crimson
}
.jsActive {
  color: orange
}
.errorClass {
  font-weight: 700;
  font-size: 30px;
}
</style>