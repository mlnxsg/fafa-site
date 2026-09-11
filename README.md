# fafa-site

fafa 的公开网页：落地页 + 隐私说明。

**这个仓库是公开的，但 fafa 的源码不在这里。** 拆成两个仓库的唯一原因是：
GitHub Pages 免费版只能给公开仓库用，而 App Store 强制要求一个公开可访问的隐私政策网址。
把网页单独拿出来，源码仓库就可以保持私有。

## 文件

| 文件 | 用途 |
|---|---|
| `index.html` | 落地页。上架后可以把 App Store 链接加上 |
| `privacy.html` | 隐私说明。**这个地址要填进 App Store Connect**，别改文件名 |

两个页面都是单文件、无依赖、无构建步骤，直接改 HTML 就行。

## 地址

开启 GitHub Pages 之后：

```
https://<你的用户名>.github.io/fafa-site/           ← 落地页
https://<你的用户名>.github.io/fafa-site/privacy.html ← 隐私说明
```

⚠️ **隐私说明的地址一旦提交给 Apple 就别再改动**（仓库改名、文件改名都会让它失效）。
审核时打不开会被直接退回。

## 以后换成自己的域名

买域名之后不用搬家：仓库根目录加一个 `CNAME` 文件写上域名，再到域名商那边配好解析，
GitHub Pages 会继续托管，地址变成 `https://你的域名/privacy.html`。
页面内容一个字都不用动。

换好之后记得同步两处：App Store Connect 里的隐私政策网址，
以及 fafa 源码里 `src/config/links.js` 的 `WEBSITE_URL`（填上就会在设置页出现「官网」一行）。
