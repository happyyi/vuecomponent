<template>
  <section :class="[panelClass,cName]">
      <h4>{{title}}</h4>
      <slot></slot>
  </section>
</template>

<script>
export default {
  props: {
    cName: {
      type: String,
      default: ""
    },
    title: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      panelClass: "panel"
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../../css/element.scss";
.panel{
    @include panel;
}
</style>


