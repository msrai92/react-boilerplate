[X] create dir and src folder w/ components and styles folder
[X] npm init - creates package.json file
[X] install webpack module bundler that lets us bundle our project files into single file for production
npm install webpack webpack-cli --save-dev (-dev will save it as dev dependency)
[X] install react and react-dom as dependency npm install react react-dom --save
[X] install babel which will transppile ES6 and JSX to ES5 npm install @babel/core babel-loader @babel/preset-env @babel/preset-react --save-dev
babel-core: transforms ES6 code to ES5
babel-loader: webpack helper to transpile code, given the preset
babel-preset-env: preset which helps babel to convert ES6, ES7, and ES8 code to ES5
babel-preset-react: preset which transforms JSX to javascript
[X] create index.js file in src folder this will be entry point for app
[X] create index.html file inside root of src folder
[X] create a webpack.config.js in root dir to define rules for our loaders
defined entry point and output dir of our app inside webpack.config.js
webpack will bundle all code from javascript files into index-bundle.js file inside the /dist dir
[X] add loaders inside webpack file which are responsible for loading and bundling source files here babel-loader is used to load JSX/Javascript files and css-loader is used to load and bundle all CSS files into one file and style-loader will add all of styles inside the style tag of the doc
[X] Before webpack can use css-loader and style-loader have to install them as dev-dependency npm install css-loader style-loader --save-dev. Webpack executes loaders from last to first (right to left)!!!!!!
[X] create .babelrc file inside root of dir to tell babel which presets to use for transpiling code here we use two presets
env: this preset is used to transpile the ES6/ES7/ES8 code to ES5
react: this preset is used to transpile JSX to code to ES5
[X] add "start": "webpack --mode development --watch", "build": "webpack --mode production" inside the script object of the package.json file here watch flag will make webpack auto compile all source files when there is a change in source files. Webpack 4 has two modes production mode and development mode the --mode flag lets us choose which mod to use
[X] npm start will compile the project after executing it a index_bundle.js file is created in the dist dir which has ES5 code that was transpiled from index.js file
[X] create App.js in components folder and App.css in styles folder
[X] modify index.js to be entry point for app
[X] install html-webpack-plugin which generetes an html file and injects script inside the html file and writes file to dis/index.html. Save as dev-dependency, npm install html-webpack-plugin --save-dev
[X] now configure webpack.config.js to require html-webpack-plugin
[X] now compile source files using webpack by running npm start
[X] install webpack dev server to refresh webpage whenever any change is made to componenets
npm install webpack-dev-server --save-dev and change script in package.json "start": "webpack-dev-server --mode development --open --hot" --open and --hot which opens and refreshes web page
[X] run npm start to run app
