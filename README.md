#cool
So I just had to lookup babel-loader on webpacks site. I needed to add two more packages and some rule loader options and plugins

1. `npm install "babel-loader@^8.0.0-beta" @babel/core @babel/preset-env webpack`
2. `npm install @babel/plugin-transform-runtime --save-dev`
3. `npm install @babel/runtime --save`

## Rules
```js
rules: [
  // the 'transform-runtime' plugin tells babel to require the runtime
  // instead of inlining it.
  {
    test: /\.js$/,
    exclude: /(node_modules|bower_components)/,
    use: {
      loader: 'babel-loader',
      options: {
        presets: ['@babel/preset-env'],
        plugins: ['@babel/plugin-transform-runtime']
      }
    }
  }
]
```
