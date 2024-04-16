# lc-vue-flex

选择器样式组件

常用场景：

- 配合 element-plus 中的 table 组件实现动态容器固定表头

## Demo

[demo](https://unpkg.com/lc-vue-flex/docs/.vitepress/dist/index.html) 

## 安装 

```
npm i lc-vue-flex 
```

## 例子

```vue
<template>
  <div>
    <p>base</p>
    <div style='width: 500px; height: 50px; border: 1px solid;'>
      <flex fit>
        <flex align-items='center' style='border: 1px solid;'>
          1
        </flex>
        <flex justify-content='center' style='border: 1px solid;'>
          2
        </flex>
        <flex justify-content='center' align-items='center' style='border: 1px solid;'>
          3
        </flex>
      </flex>
    </div>
    <p>direction='column'</p>
    <div style='width: 50px; height: 500px; border: 1px solid;'>
      <flex fit direction='column'>
        <flex align-items='center' style='border: 1px solid;'>
          1
        </flex>
        <flex justify-content='center' style='border: 1px solid;'>
          2
        </flex>
        <flex justify-content='center' align-items='center' style='border: 1px solid;'>
          3
        </flex>
      </flex>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Flex } from '@/index.ts';
</script>
```

## API

### Flex

### Attributes

| 属性名 | 说明 | 类型 | 默认值 |
| ---- | ---- | ---- | ---- |
| fit | width/height自适应 | boolean | false |
| width | 宽度 | String | - |
| height | 高度 | String | - |
| overflow | overflow | 'auto' \| 'hidden' | 'hidden' |
| display | display | 'flex' \| 'inline-flex' | 'flex' |
| direction | 同flex-direction | - | - |
| wrap | 同flex-wrap | - | - |
| basis | 同flex-basis | - | - |
| grow | 同flex-grow | - | - |
| shrink | 同flex-shrink | - | - |
| flex | 同flex | - | - |
| alignItems | 同align-items | - | - |
| justifyContent | 同justify-content | - | - |


### Slots

| 插槽名 | 说明 | 参数 |
| ---- | ---- | ---- | 
| default | 内容 | - |