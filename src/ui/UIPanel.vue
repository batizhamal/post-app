<template>
  <div class="panel">
    <slot />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.panel {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  height: $panel_height;
  max-height: 100%;
  padding: 0.4rem 1rem;
  border-bottom: 0.06rem solid #d4d4d4;
}
</style>
