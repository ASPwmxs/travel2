<template>
  <div id="app">
   <keep-alive exclude="Detail"><!-- detail组件不被缓存1 mounted -->
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
