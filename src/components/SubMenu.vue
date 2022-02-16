<template>
  <el-sub-menu :index="index" :show-timeout="0">
    <template #title><slot name="title" /></template>
    <template v-for="item in menuItems" :key="index+'-'+item.id">
      <a v-if="item.children && Array.isArray(item.children) && item.children.length" :href="item.url">
        <sub-menu :items="item.children" :index="index+'-'+item.id">
          <template #title>
            {{ item.name }}
          </template>
        </sub-menu>
      </a>
      <a v-else :href="item.url">
        <el-menu-item :index="index+'-'+item.id">
          {{ item.name }}
        </el-menu-item>
      </a>
    </template>
  </el-sub-menu>
</template>

<script>

export default {
  name: "SubMenu",
  props: ['items','index'],
  components: {},
  mounted() {
    this.menuItems = this.items
  },
  data() {
    return {
      menuItems: []
    }
  }
}
</script>

<style scoped>
</style>
