<template>
  <div class="page">
    <div class="tips">
      switch 支持左右滑动和点击进行开关操作
    </div>

    <w-group>
      <w-switch title="开关1" v-model="switchValue1"/>
      <w-switch title="开关2（禁用）" disabled v-model="switchValue2"/>
    </w-group>

    <div class="standalone-switches">
      <w-switch v-model="switchValue3" :is-in-cell="false"/>
      <w-switch v-model="switchValue4" :is-in-cell="false" disabled/>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      switchValue1: true,
      switchValue2: false,
      switchValue3: false,
      switchValue4: true
    }
  }
}
</script>

<style scoped lang="scss">
.tips {
  padding: 0.2rem 0.5rem;
  font-size: 13px;
  color: #555;
}

.standalone-switches {
  margin: 20px 0;

  .w-switch {
    margin: 10px auto;
  }
}
</style>
