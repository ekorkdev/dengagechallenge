<template>
  <div class="root">
    <div class="main">
      <left-panel></left-panel>
      <post-list></post-list>
    </div>
  </div>
</template>

<script>
import LeftPanel from "./LeftPanel.vue"
import PostList from "./PostList.vue"

export default ({
  name: 'Base',
  props: {
  },
  components: {
    LeftPanel,
    PostList
  },
  setup () {
    return {
      LeftPanel,
      PostList
    }
  }
})
</script>

<style scoped>
.main {
  height: 100vh;
  display: flex;
  flex-direction: row;
}
</style>
