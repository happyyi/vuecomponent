<template lang="html">
    <div :class="$style.home">
        <mheader></mheader>
    </div>
</template>

<script>
import mheader from "../public/header.vue";
export default {
  components: {
    mheader
  }
}
</script>

<style lang="scss" module>
  .home{
    color: red;
    font-size: 80px;
  }
</style>
