# vue-blurhash

> React components for using the [blurhash algorithm](https://blurha.sh) in your React projects

## Install
```
yarn add blurhash vue-blurhash
```

## Usage

```vue
<template>
  <Blurhash
    hash="LEHV6nWB2yk8pyo0adR*.7kCMdnj"
    :width="400"
    :height="400"
    :punch="1"
  />
</template>

<script>
import Blurhash from "vue-blurhash";

export default {
  components: {
    Blurhash,
  },
};
</script>
```

### Props

| name                     | description                                                                                                                                                                  |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `hash` (string)          | The encoded blurhash string.                                                                                                                                                 |
| `width` (int \| string)  | Width (CSS) of the decoded image.                                                                                                                                            |
| `height` (int \| string) | Height (CSS) of the decoded image.                                                                                                                                           |
| `resolutionX` (int)      | The X-axis resolution in which the decoded image will be rendered at. Recommended min. 32px. Large sizes (>128px) will greatly decrease rendering performance. (Default: 32) |
| `resolutionY` (int)      | The Y-axis resolution in which the decoded image will be rendered at. Recommended min. 32px. Large sizes (>128px) will greatly decrease rendering performance. (Default: 32) |
| `punch` (int)            | Controls the "punch" value (~contrast) of the blurhash decoding algorithm. (Default: 1)                                                                                      |

