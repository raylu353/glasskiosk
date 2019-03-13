<template>
  <div>
      <div>Hello World</div>
      <div class="info">sceen size: {{clientW}} x {{clientH}} </div>
      <div class="info">user Agent: {{userAgent}}</div>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        clientH: 0,
        clientW: 0,
        userAgent: ''
      }
    },
    mounted () {
      this.getInitInfo()
    },
    methods: {
      getInitInfo () {
        this.clientH = window.screen.height
        this.clientW = window.screen.width
        this.userAgent = navigator.userAgent
      }
    }
  }
</script>
<style land="scss" scoped>
  .info {
    font-size: 40px;
    font-weight: 600;
    -moz-transform:scaleX(-1);
    -webkit-transform:scaleX(-1);
    -o-transform:scaleX(-1);
    transform:scaleX(-1);
  }

</style>