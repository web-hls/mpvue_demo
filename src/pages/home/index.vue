<template>
  <div>
    
    <div :class="[isActive ? 'htmlActive' : '', 'errorClass']"> html绑定class </div>
    <div :class="computedClassObject"> js绑定class </div>

    <div :style="{ color : isActive ? 'green' : '' }"> html绑定style </div>
    <div :style="computedStyleObject"> style绑定style </div>

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