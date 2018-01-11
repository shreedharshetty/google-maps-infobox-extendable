# Google Maps Infobox

[This](https://github.com/lucasfs7/google-maps-infobox-module) npm module requires google maps to be loaded before initializing info box. 
If you are using webpack or browserify, it requires google maps javascript api to be loaded during the build process

Now this module will get bundled without google maps being loaded, but you need to ensure Infobox is extended with prototype methods of `google.maps.OverlayView` before initializing it.



## How to use
1. Load google maps javascript api asynchronously
2. `import {InfoBox} from 'google-maps-infobox-extendable'`
3. `extend(InfoBox.prototype, google.maps.OverlayView.prototype);`(you can write your own extend function or use [just-extend](https://www.npmjs.com/package/just-extend))

### npm
`npm install google-maps-infobox-extendable`

### yarn
`yarn add google-maps-infobox-extendable`