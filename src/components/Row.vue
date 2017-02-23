<template lang="pug">
.container
  .row.flex
    .left
      .info-container
        slot(name="left")
    .right
      .info-container
        slot(name="right")
</template>

<script>
export default {
}
</script>

<style lang="less">
</style>
