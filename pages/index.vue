<template>
  <div>
    <n-space vertical>
      <n-card title="Huge Card" size="large"> Card Content </n-card>
      <n-card title="Medium Card" size="medium"> Card Content </n-card>
    </n-space>
    <n-grid cols="2 400:1 600:2">
      <n-grid-item>
        <div class="light-green">1</div>
      </n-grid-item>
      <n-grid-item>
        <div class="green">2</div>
      </n-grid-item>
      <n-grid-item>
        <div class="light-green">3</div>
      </n-grid-item>
      <n-grid-item>
        <div class="green">4</div>
      </n-grid-item>
      <n-grid-item>
        <div class="light-green">5</div>
      </n-grid-item>
      <n-grid-item>
        <div class="green">6</div>
      </n-grid-item>
    </n-grid>
    <n-result
      status="success"
      title="succss"
      description="naive-ui now perfectly supports nuxt3"
    >
      <template #footer>
        <n-button type="success">Button</n-button>
      </template>
    </n-result>
    <n-space>
      <n-button type="primary">naive-ui</n-button>
      <n-button type="info">naive-ui</n-button>
      <n-button type="warning">naive-ui</n-button>
    </n-space>
    <n-h2>Tooltip demo</n-h2>
    <n-tooltip trigger="hover">
      <template #trigger>
        <n-button>鸭子</n-button>
      </template>
      如果它长得像鸭子，走起来像鸭子，叫起来也像鸭子，那它一定是个鸭子。
    </n-tooltip>
    <n-h1> </n-h1>
  </div>
</template>
<style>
.light-green {
  height: 108px;
  background-color: rgba(0, 128, 0, 0.12);
}
.green {
  height: 108px;
  background-color: rgba(0, 128, 0, 0.24);
}
</style>
