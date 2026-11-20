# 王羲之 · 兰亭集序

王羲之《兰亭集序》神龙本（北京故宫博物院藏） — a narrated deep-zoom reading, as a static page (in Chinese).

Wang Xizhi's Orchid Pavilion Preface, the Shenlong copy (Palace Museum, Beijing): its 28 columns, each with its modern reading beneath it, and the collectors' seals.

Live: https://youdata.github.io/lanting-xu/

The image pyramid is a tile folder (`lanting/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/lanting-xu/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → lanting-xu.json
rx export lanting-xu.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/lanting-xu --yes
```
