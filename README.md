[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg?style=flat-square)](https://www.webcomponents.org/element/gthmb/scatter-image)

# \<scatter-image\>

Applies a rendering effect to an `<img>` tag that breaks the image into pieces, scatters, and then reconsitutes them. The `<img>` tag goes in the `image` slot.

[Demo](https://www.webcomponents.org/element/gthmb/scatter-image/demo/demo/index.html)

## Default usage
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="scatter-image.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<scatter-image scatter-on-tap>
    <img slot="image" src="./demo/imgs/path.jpg">
</scatter-image>
```

## Getting fancy
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="scatter-image.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<scatter-image scatter-on-tap no-background resolution="50" composite-operation="screen">
    <img slot="image" src="./demo/imgs/train.jpg">
</scatter-image>
```

## Alt fancy
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="scatter-image.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<scatter-image scatter-on-tap resolution="8" scatter-distance="500" duration="15000">
    <img style="width: 50%;" slot="image" src="./demo/imgs/train.jpg">
</scatter-image>
```

### Configuration Attributes
| Attribute | Description | Type | Default | 
| --------- | ----------- | ---- | ------- | 
| `duration` | The time, in milliseconds, allotted for the animation to complete. | `Number` | `1000` |
| `resolution` | The size, in pixels, of the individual chunks of the image. The smaller the resolution the more chunks there are. Adjust as necessary based on image size, performance considerations and/or awesomeness | `Number` | `10` |
| `scatter-on-tap` | Enables a tap on the image or canvas to start a new scatter effect. | `Boolean` | `false` |
| `scatter-distance` | The maximum distance, in pixels, that an individual chunk will start from it's destination. | `Number` | `150` |
| `no-trails` | Will clear the canvas on each tick of the animation, which removes the the trailing effect an animating piece will leave as it moves. This generally allows the background to be more distinct during the animation. | `Boolean` | `false` |
| `no-background` | Hides the img tag during animation, removing the image as a background during the animation. | `Boolean` | `false` |
| `composite-operation` | Defines the composite operation the canvas should use to while rendering the animation. If a compositeOperation is defined, animation trails are disabled. For current valid values, @see https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation | `String` | `null` |

### Read Only, Reflected Attributes.
| Attribute | Description | Type | Default | 
| --------- | ----------- | ---- | ------- | 
| `loading` | Reflects the loading state of the image. True means the image is being loaded. | `Boolean` | `false` |
| `drawing` | Reflects the drawing state of the animation. True means the the animation is in progress. | `Boolean` | `false` |
| `complete` | Reflects if the drawing has completed | `Boolean` | `false` |

Built with Polymer 2.0
