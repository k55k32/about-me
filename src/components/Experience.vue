<template lang="pug">
.experience.flex
  .time(v-if="time") {{time}}
  .exp-desc.flex-1
    .exp-title {{title}}
    .exp-desc
      .mark(v-if="mark") {{mark}}
      slot(name="tags")
      .desc {{desc}}
      slot
</template>

<script>
export default {
  props: ['time', 'title', 'mark', 'desc']
}
</script>

<style lang="less">
.experience{
  font-weight: 100;
  .time{
    width: 100px;
  }
  .exp-title{
    font-weight: normal;
    padding-bottom: 5px;
    margin-bottom: 5px;
    border-bottom: 1px solid #ccc;
  }
  .mark{
    &:before{
      content:'职位：';
      font-style: normal;
    }
    font-style: italic;
  }
  .exp-desc{
    font-size: .95em;
    line-height: 1.5;
  }
  &{
    margin-bottom: 1.17em;
  }
}
</style>
