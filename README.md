# china-lantern

新年新气象，网站中国新年灯笼挂件

*version: 1.2*

### 效果

[效果示例](http://fz6m.github.io/china-lantern/)

![](https://cdn.jsdelivr.net/gh/fz6m/Private-picgo@moe/img/20210101051855.png)

### 使用

```html
<body>

  <!-- 在页面最后引入 -->
  <script src="https://cdn.jsdelivr.net/gh/fz6m/china-lantern@1.1/dist/china-lantern.min.js"></script>

</body>
```

### 开发

1. 安装依赖

    ```bash
      yarn
    ```

2. 在 `./src/styles` 自定义样式，在 `./build/minifier.js` 自定义灯笼文字

3. 构建

    ```bash
      yarn build
    ```
    
    之后就可以在 `./dist/china-lantern.min.js` 得到你的自定义脚本

### 其他

当你发现灯笼大小不合适或者被其他层级高的元素遮挡时，可以考虑自行修改灯笼位置的样式重新构建脚本，或者调整相关内容的 `z-index` 。

挂钩类：`.j-china-lantern`

```css
  /* 灯笼默认的 z-index: 999; */

  /* 提高灯笼的层级 */
  .j-china-lantern .lantern__warpper {
    z-index:9999;
  }

  /* 提高单个灯笼的层级：左灯笼 */
  .j-china-lantern .lantern__warpper:not(.lantern__secondary) {
    z-index:9999;
  }

  /* 提高单个灯笼的层级：右灯笼 */
  .j-china-lantern .lantern__secondary {
    z-index:9999;
  }
```
