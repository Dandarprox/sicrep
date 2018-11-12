<template>
  <div class="layout">
    <lateral-panel></lateral-panel>
    <div class="main">
      <router-view></router-view>
    </div>
  </div>  
</template>

<script>
import LateralPanel from './LateralPanel.vue'

export default {
  data() {
    return {

    }
  },
  components: {
    LateralPanel
  }
}
</script>

<style lang="sass" scoped>
@import '../styles/general.sass'

.layout
  +flex(0, 0)

.main
  flex-grow: 1
  background: radial-gradient(farthest-corner at 45px 45px , #f2e9de 0%, #f4e0c8 100%);

</style>
