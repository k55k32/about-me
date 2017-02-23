<template lang="pug">
.link.light-font
  a.link-a(:href="href", target="_blank")
    span.icon(v-if="icon") {{icon}}
    span.link-name {{name || href}}
</template>

<script>
export default {
  props: ['icon', 'href', 'name']
}
</script>

<style lang="less">
.link-group{
  display: flex;
  flex-wrap: wrap;
  .link{
    margin-right: 10px;
  }
}
.link-a{
  display: flex;
  align-items: center;
}
.link{
  margin-bottom: 10px;
  .link-name{
    flex: 1;
    overflow: hidden;
    text-overflow:ellipsis;
  }
}
.icon{
  display: flex;
  justify-content: center;
  align-items: center;
  background: darken(#eee, 10%);
  width: 20px;
  height: 20px;
  margin-right: 5px;
}
</style>
