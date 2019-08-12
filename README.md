# my-vue-library

通过vue-cli的命令进行打包，未直接配置webpack配置文件
`package.json`添加`script`
```json
"build-bundle": "vue-cli-service build --target lib --name my-vue-library ./src/components/index.js"
```
通过`files`设置要打包的文件
```json
  "files": [
    "dist/*",
    "src/*",
    "public/*",
    "*.json",
    "*.js"
  ],
```

通过`main`设置主`js`
```js
"main":"./dist/my-vue-library.common.js",
```

修改`private`为`false`
```js
"private": false,
```

### 内联css设置
在`vue.config.js`中增加
```js
module.exports = {
    ...
    css: { extract: false }
    ...
}

```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
