---
title: 扩展配置
description: Hexo Theme Solitude 的扩展配置。
---

# 扩展配置

## 控制台

```yaml
console:
  enable: false
  # Recent comments
  # 最新评论
  recentComment:
    enable: false
    # Cache time 1: 1 day / .5 : half a day
    # 缓存时间 1: 1天 / .5 : 半天
    storage: .2
  card:
    # Tags
    # 标签
    tags: true
    # Archives
    # 归档
    archive: "month" # month: by month / year: by year
```

## 右键菜单

```yaml
rightside:
  enable: false
  percent: false
  hide:
    enable: false
    translate: false
    mode: false
    aside: false
```

## 简繁转换

```yaml
translate:
  enable: true
  defaultEncoding: 2 # 1: 默认繁体 2: 默认简体
  translateDelay: 0 # 首次加载翻译迟疑时间
```

## 页脚（Footer）

:::code-group

```yaml [上方图标]
# 社交图标
information:
  author: false # img url / false
  left:
    # Github: https://github.com/everfu || fab fa-github # 名称: 链接 || 图标
    # Mail: mailto:o@everfu.org || far fa-envelope
  right:
    # Bilibili: https://space.bilibili.com/1329819902 || fab fa-bilibili
    # Douyin: https://v.douyin.com/iJsLc8jt/ || fab fa-tiktok
```

```yaml [底部导航栏]
# 底部导航栏
# Bottom navigation bar
group: # 从左至右 / From left to right
  导航:
    归档: /archives/
    分类: /categories/
    标签: /tags/
  服务:
    阿里云: https://aliyun.com/
    51la统计: https://v6.51.la/
    百度统计: https://tongji.baidu.com/
  支持:
    打赏记录: /about/
  协议:
    Cookies: /cookies/
    用户协议: /privacy/
    版权协议: /copyright/
```

```yaml [其它]
# 底部随机友链
# tip：此处的友链是随机显示的，不是固定的
# warning: 打开前必须先配置links
randomlink: false
# 备案
beian:
  # - name: 湘公网安备43048102000175号
  #   icon: https://beian.mps.gov.cn/img/logo01.dd7ff50e.png
  #   url: https://beian.mps.gov.cn/#/query/webSearch
  # - name: 湘ICP备2024080357号-1
  #   url: https://beian.miit.gov.cn/
# 页脚信息文字
links:
  # - name: RSS
  #   url: /atom.xml
  # - name: License
  #   url: https://github.com/everfu/hexo-theme-solitude/blob/main/LICENSE
  #   icon:
  #     - fas fa-copyright
  #     - fab fa-creative-commons-by
  #     - fab fa-creative-commons-nc
  #     - fab fa-creative-commons-nd
  # - name: boringbay
  #   url: https://boringbay.com/
  #   img: https://boringbay.com/api/badge/www.efu.me
```

:::

## 404 页面

> 自定义 404 页面

```yaml
errorpage:
  img: /img/404.avif
  text: =awa= Page Not Found # Text
  recommendList: true
```

## 音乐胶囊

> 显示在左下角的音乐播放器，根据注解填写对应的歌单 id 和服务商。

```yaml
capsule:
  enable: false
  # 歌单 ID / 单曲 ID
  id: 5144842535
  # 服务商：netease / qq / xiami / kugou / baidu
  server: netease
  # 类型：playlist / song
  type: playlist
  volume: 0.8
```

## 快捷菜单

```yaml
keyboard:
  enable: false
  list:
    # - name: 关闭快捷菜单
    #   key: K
    #   func: keyboard
    # - name: 打开控制台
    #   key: A
    #   sco: showConsole
    # - name: 播放/暂停音乐
    #   key: M
    #   sco: musicToggle
    # - name: 打开友链
    #   key: L
    #   url: /links/
```

## 懒加载

> 开启懒加载后，图片会在进入可视区域后加载，可以减少网页体积，提高网页加载速度。

```yaml
lazyload:
  enable: false
  # post, site
  field: site
  # 加载时替换图
  placeholder: ""
  # 加载失败替换图
  errorimg: /img/error_load.avif
```

## 加载动画

> 在页面加载时会显示一个页面覆盖内容，加载完成消失。

```yaml
loading:
  # 全屏加载
  fullpage: false
  # 加载图标，不写默认siteicon
  favicon: /img/favicon.png
  # Pace 加载
  pace: true
```

## 代码高亮

> 开启代码高亮后，代码块会有对应的语言提示，但是会增加网页体积，如果你不需要这个功能，可以关闭。

```yaml
highlight:
  enable: true
  # 当超过多少字时显示折叠按钮
  limit: 200
  # 是否启用复制按钮
  copy: true
  # 是否默认展开
  expand: true
  # default: 默认 / mac : 苹果终端
  theme: mac
  # default / solidity / dracula
  color: default
```

## 图片灯箱

> fancybox 和 mediumZoom 二选一，一定要关闭 fancybox 才能开启 mediumZoom

```yaml
# image lightbox
lightbox: true # 是否开启图片灯箱

# fancybox
# https://fancyapps.com/fancybox/
fancybox: true

# mediumZoom
mediumZoom: false
```

## 纪念日

网站整体变灰

```yaml
memorial:
  enable: false
  date:
  #  - 7-7
  #  - 9-18
  #  - 12-13
```

## Open graph

> 开启后，网站会自动添加 Open Graph 标签，用于社交分享。

```yaml
# Open Graph
# https://ogp.me/
# https://developers.facebook.com/docs/sharing/webmasters/
Opengraph:
  enable: false
  options:
    # twitter_card:
    # twitter_image:
    # twitter_id:
    # twitter_site:
    # google_plus:
    # fb_admins:
    # fb_app_id:
```

## 字数统计

> 需要安装 `hexo-wordcount` 插件。

```yaml
# 字数统计
# warning：开启前需要安装字数统计插件
wordcount: false
```

## Busuanzi

```yaml
busuanzi: false
# 0: 原版 / 1: 自定义版
busuanzi_use: 0
```

## 数学公式

> 请查看作者文章：[Theme: 渲染器 markdown-it](https://www.efu.me/posts/941787ac.html)

主题支持使用 **Latex** 数学公式 当需要使用数学公式时，在文章的 **Front-Matter** 添加。

## 站点验证

```yaml
# 站点验证
# Site verification
# 仅需要填写验证代码即可，譬如：codeva-KReTIJu5us
# Only need to fill in the verification code, such as: codeva-KReTIJu5us
verify_site:
  # - name: google-site-verification
  #   content: xxxxxx
  # - name: baidu-site-verification
  #   content: xxxxxxx
```

## CSS 前缀

```yaml
# CSS 前缀
# CSS prefix
# 有些 CSS 并不是所有浏览器都支持，需要增加对应的前缀才会生效
# Some CSS is not supported by all browsers, and you need to add the corresponding prefix to take effect
# 开启 css_prefix 后，会自动为一些 CSS 增加前缀。（会增加 20%的体积）
# After opening css_prefix, some CSS will be automatically prefixed. (Will increase 20% of the volume)
css_prefix: false
```

## Inject

```yaml
# 插入代码到头部 </head> 之前 和 底部 </body> 之前
# Insert code before </head> and before </body>
# 插入额外代码 如：统计，广告等
# Insert additional code such as: statistics, advertising, etc.
extends:
  head:# 在head中插入 / Insert in head
    # - <script src="https://cdn.bootcdn.net/ajax/libs/pace/1.2.4/pace.min.js"></script>
  body: # 在body中插入 / Insert in body
```

## PWA

PWA 全称为 Progressive Web App，中文译为渐进式 Web APP，其目的是通过各种 Web 技术实现与原生 App 相近的用户体验。纵观现有 Web 应用与原生应用的对比差距，如离线缓存、沉浸式体验等等，可以通过已经实现的 Web 技术去弥补这些差距，最终达到与原生应用相近的用户体验效果。

[SWPP 官方文档 & 项目地址](https://github.com/EmptyDreams/swpp-backends)

1. 安装插件
   ```bash
   npm install hexo-swpp swpp-backends --save
   ```
2. 开启主题配置
   ```yaml
   # PWA
   # https://developer.mozilla.org/zh-CN/docs/Web/Progressive_web_apps
   # docs: https://solitude.js.org/config/extra#pwa
   pwa:
     enable: false
     manifest: /manifest.json # manifest.json 文件路径
     theme_color: "#006a73" # 主题颜色
     mask_icon: /img/pwa/favicon.ico # 遮罩图标
     apple_touch_icon: /img/pwa/favicon.ico # 苹果触摸图标
     bookmark_icon: /img/pwa/favicon.ico # 书签图标
     favicon_32_32: /img/pwa/favicon_32.ico # 32x32图标
     favicon_16_16: /img/pwa/favicon_16.ico # 16x16图标
   ```
3. 在项目根目录新建 `sw-rules.js` 加入以下内容。

   **提供一个 SWPP 文件**

   ```js
   module.exports.config = {
     /** @type {?ServiceWorkerConfig|boolean} */
     serviceWorker: {
       escape: 0,
       cacheName: "SolitudeCache",
       debug: false,
     },
     register: {
       onsuccess: undefined,
       onerror: () =>
         console.error(
           "Service Worker 注册失败！可能是由于您的浏览器不支持该功能！"
         ),
       builder: (root, framework, pluginConfig) => {
         const { onerror, onsuccess } = pluginConfig.register;
         return `
               <script>
                   (() => {
                       const sw = navigator.serviceWorker;
                       const error = ${onerror && onerror.toString()};
                       if (!sw?.register('${new URL(root).pathname}sw.js')
                           ${onsuccess ? `?.then(${onsuccess.toString()})` : ""}
                           ?.catch(error)
                       ) error()
                   })()
               </script>`;
       },
     },
     /** @type {?DomConfig|boolean} */
     dom: {
       /** @type {?VoidFunction} */
       onsuccess: () => {
         caches
           .match(location.href)
           .then((res) => {
             if (res)
               res.json().then((json) => {
                 utils &&
                   utils.snackbarShow(
                     `已刷新缓存，更新为${
                       json.global + "." + json.local
                     }版本最新内容`,
                     false,
                     2000
                   );
               });
             else console.info("未找到缓存");
           })
           .catch((error) => console.error("缓存匹配出错", error));
       },
     },
     /** @type {?VersionJsonConfig|boolean} */
     json: {
       /** @type {number} */
       maxHtml: 15,
       /** @type {number} */
       charLimit: 1024,
       /** @type {string[]} */
       merge: [],
       exclude: {
         /** @type {RegExp[]} */
         localhost: [],
         /** @type {RegExp[]} */
         other: [],
       },
     },
     /** @type {?ExternalMonitorConfig|boolean} */
     external: {
       /** @type {number} */
       timeout: 5000,
       /** 拉取文件时地并发限制 */
       concurrencyLimit: 100,
       /** @type {({head: string, tail: string}|function(string):string[])[]} */
       js: [],
       /** @type {RegExp[]} */
       stable: [
         /^https:\/\/npm\.elemecdn\.com\/[^/@]+\@[^/@]+\/[^/]+\/[^/]+$/,
         /^https:\/\/cdn\.cbd\.int\/[^/@]+\@[^/@]+\/[^/]+\/[^/]+$/,
         /^https:\/\/cdn\.jsdelivr\.net\/npm\/[^/@]+\@[^/@]+\/[^/]+\/[^/]+$/,
       ],
       replacer: (srcUrl) => {
         if (srcUrl.startsWith("https://cdn.jsdelivr.net/npm/")) {
           const pathname = new URL(srcUrl).pathname;
           return [
             srcUrl,
             `https://cdn.cbd.int/${pathname}`,
             `https://npm.elemecdn.com/${pathname}`,
             `https://fastly.jsdelivr.net/npm/${pathname}`,
           ];
         } else {
           return srcUrl;
         }
       },
     },
   };

   module.exports.cacheRules = {
     simple: {
       clean: true,
       search: false,
       match: (url, $eject) =>
         url.host === $eject.domain && ["/404.html"].includes(url.pathname),
     },
     cdn: {
       clean: true,
       match: (url) =>
         [
           "cdn.cbd.int",
           "lf26-cdn-tos.bytecdntp.com",
           "lf6-cdn-tos.bytecdntp.com",
           "lf3-cdn-tos.bytecdntp.com",
           "lf9-cdn-tos.bytecdntp.com",
           "cdn.staticfile.org",
           "npm.elemecdn.com",
         ].includes(url.host) &&
         url.pathname.match(/\.(js|css|woff2|woff|ttf|cur)$/),
     },
   };

   module.exports.getSpareUrls = (srcUrl) => {
     if (srcUrl.startsWith("https://npm.elemecdn.com")) {
       return {
         timeout: 3000,
         list: [
           srcUrl,
           `https://fastly.jsdelivr.net/${new URL(srcUrl).pathname}`,
         ],
       };
     }
   };

   module.exports.ejectValues = (hexo, rules) => {
     return {
       domain: {
         prefix: "const",
         value: new URL(hexo.config.url).host,
       },
     };
   };

   module.exports.skipRequest = (request) =>
     request.url.startsWith("https://i0.hdslb.com") ||
     request.url.startsWith("https://meting.qjqq.cn") ||
     request.url.startsWith("https://api.i-meto.com");
   ```

4. 根据需求在 `source` 文件夹下新建 `manifest.json` 文件并增加内容，以下是示例：
   ```json
   {
     "name": "放养平凡",
     "short_name": "BTA",
     "theme_color": "#b00000",
     "background_color": "#b00000dd",
     "description": "世界为你简单",
     "display": "fullscreen",
     "scope": "/",
     "start_url": "/",
     "lang": "zh-CN",
     "id": "/",
     "icons": [
       {
         "src": "pwa/16.ico",
         "sizes": "16x16",
         "type": "image/png",
         "purpose": "any"
       },
       {
         "src": "pwa/16.ico",
         "sizes": "16x16",
         "type": "image/png",
         "purpose": "maskable"
       },
       {
         "src": "pwa/32.ico",
         "sizes": "32x32",
         "type": "image/png",
         "purpose": "any"
       },
       {
         "src": "pwa/32.ico",
         "sizes": "32x32",
         "type": "image/png",
         "purpose": "maskable"
       },
       {
         "src": "pwa/64.ico",
         "sizes": "64x64",
         "type": "image/png",
         "purpose": "any"
       },
       {
         "src": "pwa/64.ico",
         "sizes": "64x64",
         "type": "image/png",
         "purpose": "maskable"
       },
       {
         "src": "pwa/128.ico",
         "sizes": "128x128",
         "type": "image/png",
         "purpose": "any"
       },
       {
         "src": "pwa/128.ico",
         "sizes": "128x128",
         "type": "image/png",
         "purpose": "maskable"
       },
       {
         "src": "pwa/256.ico",
         "sizes": "256x256",
         "type": "image/png",
         "purpose": "any"
       },
       {
         "src": "pwa/256.ico",
         "sizes": "256x256",
         "type": "image/png",
         "purpose": "maskable"
       }
     ],
     "screenshots": [
       {
         "src": "https://assets.btwoa.com/blogbtwoacom.avif",
         "sizes": "1920x1080",
         "type": "image/png",
         "form_factor": "wide",
         "label": "Fullscreen of BTA"
       },
       {
         "src": "https://assets.btwoa.com/darkblogbtwoacom.avif",
         "sizes": "1920x1080",
         "type": "image/png",
         "form_factor": "wide",
         "label": "Fullscreen of BTA"
       }
     ],
     "splash_pages": null
   }
   ```

## CDN

主题资源已经被 cdnjs 收录，所以大家可以放心食用，如果你有自己的 CDN，可以自定义配置。

```yaml
# CDN
# Don't modify the following settings unless you know how they work
# 非必要请不要修改
CDN:
  # The CDN provider of internal scripts (主题内 js 的 cdn 配置)
  # option: local.md/jsdelivr/unpkg/cdnjs/custom
  # Dev version can only choose. ( dev版本只能为 local.md )
  internal: local.md
  # The CDN provider of third party scripts (第三方 js 的 cdn 配置)
  # option: jsdelivr/unpkg/cdnjs/custom
  third_party: custom

  # Add version number to url, true or false
  version: true

  # Custom format
  # For example: https://cdn.staticfile.net/${cdnjs_name}/${version}/${min_cdnjs_file}
  custom_format: https://cdn.staticfile.net/${cdnjs_name}/${version}/${min_cdnjs_file}

  option:
    solitude_css: https://cdn2.codesign.qq.com/icons/7pOrz0WXB5ZWJPX/latest/iconfont.css
    # algolia_search:
    # instantsearch:
    # pjax:
    # twikoo:
    # waline_js:
    # waline_css:
    # sharejs:
    # sharejs_css:
    # katex:
    # katex_copytex:
    # lazyload:
    # aplayer_css:
    # aplayer_js:
    # meting_js:
    # pace_js:
    # swiper_css:
    # swiper_js:
    # busuanzi_js:
    # snackbar_js:
```
