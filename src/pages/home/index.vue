<template>
  <div>
    
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
export default {
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