# Hexo-one-piece
 - 后端狗一枚，审美有限，基于 [hexo-theme-shoka](https://github.com/amehime/hexo-theme-shoka) 定制，主要替换为海贼王元素，非常感谢@amehime，主题很漂亮；
 - 这个项目是模版工程，下载后可以直接使用，具备完整的hexo生命周期。
 - 不定时更新，更新内容多为深度主题定制、缺陷修复和功能优化；

---

# 准备工作
1. 需要具备hexo引擎环境；
   - 需要安装node环境，[官网链接](https://nodejs.org/en/) ，推荐安装yarn,`npm install --global yarn`
   - 安装hexo引擎，`npm install hexo-cli -g` 
2. clone代码并运行
   - 安装依赖，`yarn or npm install `
   - 测试运行，`hexo g` and `hexo server`
   - default url : 'localhost:4000'

# 内容调整/依赖说明
## base on "hexo-6.1.0" 
- 

## 插件作用及说明：

| 插件名称                            | 功能描述                  | 当前状态 |
|---------------------------------|-----------------------|------|
| hexo-renderer-multi-markdown-it | md文件渲染器，压缩css/js/html | 已配置  |
| hexo-autoprefixer               | 给生成的css文件们添加浏览器前缀     | 已配置  |
| hexo-algoliasearch              | 站内搜索功能                | 已配置  |
| hexo-symbols-count-time         | 文章或站点字数及阅读时间统计        | 已配置  |
| hexo-feed                       | 生成Feed文件              | 已配置  |

> 特别说明1：
>>  hexo-renderer-multi-markdown-it ： 插件是原作者自己封装的package，依赖了prismjs，和markdown-it的很多依赖。
>>  因为现在hexo也提供了prismjs支持，所以如果出现以下提示：
>>  `Prism's Diff Highlight plugin requires the Diff language definition (prism-diff.js).Make sure the language definition is loaded or use Prism's Autoloader plugin.`
>>  需要去Prism官网下载依赖信息，依赖node_modules/prismjs下prismjs文件，我就不额外引入prismjs的依赖配置了。

> 特别说明2：
>>  如果出现 circular dependency，已知的为：nib这个包里的 stylus 引起的问题和 hexo-renderer-stylus 版本冲突。
>>  use `npx cross-env NODE_OPTIONS="--trace-warnings" hexo s` to show warning stack info.

# 其他配置说明
- iconfont配置  : https://www.iconfont.cn/

# 部署操作
