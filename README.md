# verbose-barnacle
[Souvik Sarkar] Using Vue.js To Create An Interactive Weather Dashboard With APIs

Grab the article at [https://www.smashingmagazine.com/2019/02/interactive-weather-dashboard-api-vue-js/](https://www.smashingmagazine.com/2019/02/interactive-weather-dashboard-api-vue-js/)

## Tips/Run

* "npm install -g vue@latest vue-cli@latest" (Installing latest 'Vue' and 'Vue-Cli' packages);
* "vue init webpack-simple verbose-barnacle" (Initialising a new 'webpack-simple' templated Vue project);
* "cd verbose-barnacle", "npm install", "npm run dev" (Getting the started with pre-installation and first build run);
* "npm audit", "npm audit fix", "npm install --save-dev webpack-dev-server@latest", "npm install --save-dev css-loader@latest", "npm install --save-dev webpack@latest", "npm i -D webpack-cli" (Auditing the package vulnerabilities and fixing said packages);

## Errors Experienced

* Upon initialising, audit fixing, and running, the following error occurred on running the first dev build:
-"ERROR in ./src/App.vue
Module build failed (from ./node_modules/vue-loader/index.js):
TypeError: Cannot read property 'vue' of undefined
    at Object.module.exports (G:\git\Source\Repos\verbose-barnacle\verbose-barnacle\node_modules\vue-loader\lib\loader.js:61:18)
 @ ./src/main.js 2:0-28 7:13-16"
* In trying to eradicate the problem, the installation - "npm install --save-dev vue-loader@latest" errored in the following fashion:
-"ERROR in ./src/App.vue
Module Error (from ./node_modules/vue-loader/lib/index.js):
vue-loader was used without the corresponding plugin. Make sure to include VueLoaderPlugin in your webpack config.
 @ ./src/main.js 2:0-28 7:13-16

ERROR in ./src/App.vue?vue&type=style&index=0&lang=css& 34:0
Module parse failed: Unexpected character '#' (34:0)
File was processed with these loaders:
 * ./node_modules/vue-loader/lib/index.js
You may need an additional loader to handle the result of these loaders.
|
|
> #app {
|   font-family: 'Avenir', Helvetica, Arial, sans-serif;
|   -webkit-font-smoothing: antialiased;
 @ ./src/App.vue 4:0-63
 @ ./src/main.js

ERROR in ./src/App.vue?vue&type=template&id=7ba5bd90& 2:0
Module parse failed: Unexpected token (2:0)
File was processed with these loaders:
 * ./node_modules/vue-loader/lib/index.js
You may need an additional loader to handle the result of these loaders.
|
> <div id="app">
|   <img src="./assets/logo.png">
|   <h1>{{ msg }}</h1>
 @ ./src/App.vue 1:0-82 11:2-8 12:2-17 31:4-36:6 31:66-36:5 33:16-22 34:25-40
 @ ./src/main.js"
* On a GitHub page it was suggested that an earlier version - 14.2.2 - would help fix the issue for this build (15.9.3), thus installing - "npm install --save-dev vue-loader@^14.2.2" - has fixed the immediate problem; running "npm install" followed by "npm run dev" has provided me with my initial project;

## Notes:

* "One important thing before we move on — the URL for the Google Maps API contains a key which is a property of FusionCharts. For now, you can use this key to build the project, as we don’t want you to get bogged down by these type of minute details (which can be distractions while you are new). However, we strongly urge you to generate and use your own Google Maps API key once you have made some progress and feel comfortable to pay attention to these tiny details.";
* Adding 'Vue.js devtools' to Chrome for a suitable debug environment;
* Interesting injecting/rendering of properties under 'props' ([https://vuejs.org/v2/guide/components-props.html](https://vuejs.org/v2/guide/components-props.html));

## What's it all about?

* Creating a dashboard with API data is often a complex affair. Choosing your tech stack, integrating APIs, selecting the right charts and beautifying with CSS styles can become tricky. This tutorial is a step-by-step guide on how to help you create a weather dashboard in Vue.js using API data

## Thanks

Thanks goes out to Souvik Sarkar for the FREE stuff!

* [Souvik Sarkar's SmashingMagazine profile](https://www.smashingmagazine.com/author/souvik-sarkar) ...Souvik works as a Technical Writer at FusionCharts, and has a background in back-end technologies and databases...
