# pixi-live2d

Display live2D model as a sprite in [pixi.js](https://github.com/pixijs/pixi.js).

--------------------------------------------------------------------------------

[Installation](#Installation) | [Example](#Example) | [API](#API) | [License](#License) | [Donation](#Donation)

Pixi-live2d is a plugin for pixi.js for displaying live2D model as a sprite in pixi.js.

- Only available in WebGL
- ECMAScript 2015+
- [Have a look at example!](https://avgjs.github.io/pixi-live2d/)
- [Make me know](mailto:bingfeng.web@gmail.com?subject=Hey,%20I%20made%20a%20cool%20work%20with%20your%20plugin!) if you use my plugin for cool things!

## Installation

```bash
npm install pixi-live2d
```

## Example

```javascript
import PIXI from 'pixi.js';
import 'pixi-live2d';

const renderer = new PIXI.WebGLRenderer(800, 600);
document.body.appendChild(renderer.view);
const stage = new PIXI.Container();

const live2dSprite = new PIXI.Live2DSprite(modelHaru);
stage.addChild(live2dSprite);

live2dSprite.startRandomMotion('idle');
live2dSprite.on('mousemove', (evt) => {
  const point = evt.data.global;
  live2dSprite.setViewPoint(point.x, point.y);
});

function animate() {
    requestAnimationFrame(animate);
    renderer.render(stage);
}
animate();
```

You can find a more complex one at [`example` folder](./example), or [visit it online](https://avgjs.github.io/pixi-live2d/).

## API

<docs/API.md>

## License

This plugin is distributed under MIT license, and you should agree with the licenses of Live2D and pixi.js.

For more detail, please read <LICENSE.txt>.

## Donation

The plugin is free for charge, if you like it don't forget to buy me a coffee!

ko-fi:<br>
[![Buy Me a Coffee at ko-fi.com](https://az743702.vo.msecnd.net/cdn/kofi4.png?v=b)](https://ko-fi.com/A742BTX)

alipay:<br>
![](https://cloud.githubusercontent.com/assets/837432/19645521/a71da460-9a27-11e6-9605-aed9e251dd7a.png)