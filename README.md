# DeepReview
> 你想的，我们都有

## 技术支持
* ES2015 + 
* webpack2+
* vue2+
* 多页，dll
* [配置目录说明](config/README.md)

## 注意事项 && 解决一些ＢＵＧ
* add-asset-html-webpack-plugin 插件修复 `outpath` 支持
* 修复DllPlugin + CommonChunkPlugin 一起使用时，会导致`Uncaught TypeError: Cannot read property 'call' of undefined`的BUG
* 新增 mock-server 模块扩展，移除Resetful API规则，更新请解压`node_modules`

## 开始工作

```javascript
$> npm run dll
```

2.接下来你可以尽情使用vue2,以及webpack2 + ES2015 的特性

**开启Mock服务**
```javascript
$> npm run mock
```

**启动开发服务器**
```javascript
$> npm run dev
```

**编译代码**
```javascript
$> npm run compile
```

### 细节
src 目录结构
```html
    src
    ├─assets                   ## 第三方资源
    │  ├─common
    │  └─lib
    ├─components               ## 通用组件
    ├─pages                    ## 多页存放
    │  ├─as
    │  │  └─components         ## 私有组件
    │  └─workIndex
    │      └─components
    ├─styles                   ## 通用样式
    │  ├─fonts
    │  ├─imgs
    │  └─variables
    └─templates                ## 通用模板
        └─common
```
compile 后 dist 目录结构
```html
    dist
    ├─assets
    │  ├─common
    │  └─lib
    ├─css
    │  ├─as
    │  └─workIndex
    ├─dll
    ├─fonts
    ├─images
    ├─js
    │  ├─as
    │  └─workIndex
    └─pages
        ├─as
        └─workIndex
```
