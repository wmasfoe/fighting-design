# Radio 单选框

你只有一个选择

- [源代码](https://github.com/FightingDesign/fighting-design/tree/master/packages/fighting-design/radio)
- [文档编辑](https://github.com/FightingDesign/fighting-design/blob/master/docs/docs/components/radio.md)

## 基本使用

需要使用 `v-model` 绑定一个值

::: demo

```vue
<script lang="ts" setup>
  import { ref } from 'vue'

  const radio = ref('1')
</script>

<template>
  <f-radio-group v-model="radio">
    <f-radio label="1">备选项1</f-radio>
    <f-radio label="2">备选项2</f-radio>
    <f-radio label="3">备选项3</f-radio>
  </f-radio-group>
</template>
```

:::

## 带有边框

`border` 属性可以配置带有边框的效果

::: demo

```vue
<script lang="ts" setup>
  import { ref } from 'vue'

  const radio = ref('1')
</script>

<template>
  <f-radio-group v-model="radio" border>
    <f-radio label="1">备选项1</f-radio>
    <f-radio label="2">备选项2</f-radio>
    <f-radio label="3">备选项3</f-radio>
  </f-radio-group>
</template>
```

:::

## 不同尺寸

`size` 属性可以配置不同的尺寸

::: demo

```vue
<script lang="ts" setup>
  import { ref } from 'vue'

  const radio = ref('1')
</script>

<template>
  <f-space vertical>
    <f-radio-group v-model="radio" border size="large">
      <f-radio label="1">备选项1</f-radio>
      <f-radio label="2">备选项2</f-radio>
      <f-radio label="3">备选项3</f-radio>
    </f-radio-group>

    <f-radio-group v-model="radio" border size="middle">
      <f-radio label="1">备选项1</f-radio>
      <f-radio label="2">备选项2</f-radio>
      <f-radio label="3">备选项3</f-radio>
    </f-radio-group>

    <f-radio-group v-model="radio" border size="small">
      <f-radio label="1">备选项1</f-radio>
      <f-radio label="2">备选项2</f-radio>
      <f-radio label="3">备选项3</f-radio>
    </f-radio-group>

    <f-radio-group v-model="radio" border size="mini">
      <f-radio label="1">备选项1</f-radio>
      <f-radio label="2">备选项2</f-radio>
      <f-radio label="3">备选项3</f-radio>
    </f-radio-group>
  </f-space>
</template>
```

:::

## 纵向排列

`vertical` 属性可以纵向排列

::: demo

```vue
<script lang="ts" setup>
  import { ref } from 'vue'

  const radio = ref('1')
</script>

<template>
  <f-radio-group v-model="radio" vertical>
    <f-radio label="1">备选项1</f-radio>
    <f-radio label="2">备选项2</f-radio>
    <f-radio label="3">备选项3</f-radio>
  </f-radio-group>
</template>
```

:::

## 禁用状态

`disabled` 属性可以禁用指定选项，作用在 `f-radio-group` 组件上可以全部禁用，作用在 `f-radio` 上可以指定禁用某一项

::: demo

```vue
<script lang="ts" setup>
  import { ref } from 'vue'

  const radio = ref('1')
</script>

<template>
  <f-space vertical>
    <f-radio-group v-model="radio" disabled>
      <f-radio label="1">备选项1</f-radio>
      <f-radio label="2">备选项2</f-radio>
      <f-radio label="3">备选项3</f-radio>
    </f-radio-group>

    <f-radio-group v-model="radio">
      <f-radio label="1">备选项1</f-radio>
      <f-radio label="2" disabled>备选项2</f-radio>
      <f-radio label="3">备选项3</f-radio>
    </f-radio-group>
  </f-space>
</template>
```

:::

## RadioGroup Attributes

| 参数                   | 说明                   | 类型                                                               | 可选值                          | 默认值 |
| ---------------------- | ---------------------- | ------------------------------------------------------------------ | ------------------------------- | ------ |
| `modelValue / v-model` | 绑定值                 | <a href="#radiomodelvalue">RadioModelValue</a>                     | ——                              | ——     |
| `disabled`             | 是否禁用               | boolean                                                            | ——                              | false  |
| `vertical`             | 是否纵向排列           | boolean                                                            | ——                              | false  |
| `column-gap`           | 横向排列的间距         | string / number                                                    | ——                              | ——     |
| `row-gap`              | 纵向排列的间距         | string / number                                                    | ——                              | ——     |
| `border`               | 是否显示边框           | boolean                                                            | ——                              | false  |
| `size`                 | 尺寸                   | <a href="/components/interface.html#fightingsize">FightingSize</a> | `large` `middle` `small` `mini` | middle |
| `on-change`            | 绑定值变化时触发的回调 | <a href="#radiochange">RadioChange</a>                             | ——                              | ——     |

## Radio Attributes

| 参数                   | 说明                   | 类型                                           | 可选值 | 默认值  |
| ---------------------- | ---------------------- | ---------------------------------------------- | ------ | ------- |
| `modelValue / v-model` | 绑定值                 | <a href="#radiomodelvalue">RadioModelValue</a> | ——     | ——      |
| `disabled`             | 是否禁用               | boolean                                        | ——     | false   |
| `name`                 | 自定义 name            | string                                         | ——     | f-radio |
| `label`                | 单选框对应的值         | <a href="#radiomodelvalue">RadioModelValue</a> | ——     | ——      |
| `on-change`            | 绑定值变化时触发的回调 | <a href="#radiochange">RadioChange</a>         | ——     | ——      |

## RadioGroup Slots

| 名称      | 说明           |
| --------- | -------------- |
| `default` | 插入 `f-radio` |

## Radio Slots

| 名称      | 说明           |
| --------- | -------------- |
| `default` | 单选框对应的值 |

## Interface

组件导出以下类型定义：

```ts
import type {
  RadioInstance,
  RadioProps,
  RadioGroupInstance,
  RadioGroundProps,
  RadioModelValue,
  RadioChange
} from 'fighting-design'
```

### RadioModelValue

```ts
type RadioModelValue = string | number | boolean
```

### RadioChange

```ts
type RadioChange = (value: RadioModelValue) => void
```

## Contributors

<a href="https://github.com/Tyh2001" target="_blank">
  <f-avatar round src="https://avatars.githubusercontent.com/u/73180970?v=4" />
</a>

<a href="https://github.com/tangtts" target="_blank">
  <f-avatar round src="https://avatars.githubusercontent.com/u/50451042?v=4" />
</a>