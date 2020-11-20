<template>
  <div id="app">
    <!-- <div class="btn btn-primary">{{key}}</div> -->
    <de-mo></de-mo>
  </div>
</template>
<script>
  import deMo from '@/components/demo.vue';
export default{
  components: {
    deMo
  },
  data() {
    return {
      key: 'TEST'
    }
  },

}
</script>
<style>

</style>
