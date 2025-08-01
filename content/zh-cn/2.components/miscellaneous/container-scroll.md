---
title: Container Scroll
description: A container scrolling effect that transforms the content inside based on scroll progress. Features smooth transitions with scaling and rotating effects on scroll.
---

::ComponentLoader{label="预览" componentName="ContainerScrollDemo" type="examples"}  
::

## 通过 CLI 安装

::InstallationCli{componentId="container-scroll"}
::

## 手动安装

在同一个文件中，复制并粘贴以下代码：

::code-group

:CodeViewerTab{label="ContainerScroll.vue" language="vue" componentName="ContainerScroll" type="ui" id="container-scroll"}
:CodeViewerTab{label="ContainerScrollTitle.vue" language="vue" componentName="ContainerScrollTitle" type="ui" id="container-scroll"}
:CodeViewerTab{label="ContainerScrollCard.vue" language="vue" componentName="ContainerScrollCard" type="ui" id="container-scroll"}

::

## API

::steps

### `ContainerScroll`

The `ContainerScroll` component creates a 3D scroll effect. As the user scrolls, the content inside the container is transformed with scale, rotation, and translation effects.

#### Props

| Prop 名称    | 类型   | 默认值 | 描述                                                                          |
| ------------ | ------ | ------ | ----------------------------------------------------------------------------- |
| `rotate`     | Number | `0`    | Controls the rotation of the inner content based on the scroll progress.      |
| `scale`      | Number | `1`    | Controls the scaling transformation applied to the content during the scroll. |
| `translateY` | Number | `0`    | Controls the vertical translation of the title during the scroll.             |

#### 用例

```vue [ContainerScroll.vue]
<ContainerScroll :rotate="rotateValue" :scale="scaleValue" :translateY="translateYValue">
  <template #title>
    <!-- Your title content here -->
  </template>
  <template #card>
    <!-- Your card content here -->
  </template>
</ContainerScroll>
```

### `ContainerScrollTitle`

The `ContainerScrollTitle` component handles the title's transformation as the user scrolls, applying a vertical translation effect.

#### Props

| Prop 名称   | 类型   | 默认值 | 描述                                            |
| ----------- | ------ | ------ | ----------------------------------------------- |
| `translate` | Number | `0`    | Controls the vertical translation of the title. |

#### 用例

```vue [ContainerScrollTitle.vue]
<ContainerScrollTitle :translate="translateYValue">
  <!-- Title content here -->
</ContainerScrollTitle>
```

### `ContainerScrollCard`

The `ContainerScrollCard` component applies scale and rotation effects to the card content as the user scrolls through the page.

#### Props

| Prop 名称 | 类型   | 默认值 | 描述                                             |
| --------- | ------ | ------ | ------------------------------------------------ |
| `rotate`  | Number | `0`    | Controls the rotation effect of the card.        |
| `scale`   | Number | `1`    | Controls the scaling effect applied to the card. |

#### 用例

```vue [ContainerScrollCard.vue]
<ContainerScrollCard :rotate="rotateValue" :scale="scaleValue">
  <!-- Card content here -->
</ContainerScrollCard>
```

::

## 功能特性

- **3D Scroll Effects**: The content transforms based on scroll progress, including rotation, scaling, and translation.
- **Responsive Design**: Adjusts behavior dynamically for mobile and desktop views.
- **Smooth Transitions**: Leverages CSS keyframes and scroll-based transformations for a fluid user experience.

## CSS Variables

To customize the scroll animations and responsiveness, you can set the following CSS variables:

- **`--scale-start`**: Initial scale value for the card.
- **`--scale-end`**: Final scale value for the card as the scroll progresses.
- **`--rotate-start`**: Initial rotation value for the card.
- **`--rotate-end`**: Final rotation value for the card as the scroll progresses.

## 功能特性

- **Dynamic Transformations**: Based on scroll position, the content scales, rotates, and translates for a 3D effect.
- **Flexible Content**: Place any custom content inside the title and card slots.
- **Responsive**: Adjusts for mobile and desktop, providing a consistent experience across devices.

## 感谢

- Inspired by [Aceternity UI Container Scroll Animation](https://ui.aceternity.com/components/container-scroll-animation).
