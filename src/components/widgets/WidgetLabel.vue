<template>
  <vue-interactjs
    :widget=widget
    :minw="100"
    :minh="30"
  >
    <div class="outer">
      <div class="inner"
        :style="{color: widget.c, backgroundColor: widget.bc, textAlign: widget.a}"
      >
        <span>{{ widget.t }}</span>
      </div>
    </div>
  </vue-interactjs>
</template>

<script>

  import VueInteractjs from '../../helpers/vue-interactjs'

  export default {
    props: [ 'widget' ],

    components: {
      'vue-interactjs': VueInteractjs
    }
  }

</script>

<style lang=scss scoped>

  .outer {
    display: table;
    width: 100%;
    height: 100%;

    .inner {
      padding: 10px;
      display: table-cell;
      vertical-align: middle;
      text-align: center;
      font-family: 'Delius', serif;
      font-size: 18px;
      line-height: 20px;
      padding: 0;
    }
  }

</style>
