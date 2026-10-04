# clorf.top

个人主页（GitHub Pages 用户站点 `clorf6.github.io`，自定义域名 `clorf.top`）。
目前只放 CV，主页之后再搭。

| 地址 | 内容 |
| --- | --- |
| `clorf.top/` | 暂时跳转到 blog.clorf.top |
| `clorf.top/CV` | 跳转到 `/CV.pdf` |
| `clorf.top/CV.pdf` | CV 本体 |

GitHub Pages 会把 `/CV` 解析到 `CV.html`，但它不能做服务端重写，
所以 `CV.html` 用 meta refresh 跳到 PDF，由浏览器自带的 PDF 阅读器打开
（比把 PDF 嵌进 iframe 在手机上靠谱）。线上路径区分大小写，`/cv` 会 404；
Windows 上 `CV.html` 与 `cv.html` 又是同一个文件，没法两份并存。

## 更新 CV

用新文件覆盖 `CV.pdf`（文件名保持不变），然后：

```bash
git add CV.pdf
git commit -m "update CV"
git push
```

GitHub Pages 缓存约 10 分钟，之后生效。

注意：仓库是公开的，旧版本 CV 会一直留在 git 历史里。
