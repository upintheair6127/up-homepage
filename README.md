# 出海者Neal 个人主页

静态单页，给 GitHub Pages 用。只有 HTML、CSS 和原生 JavaScript，不需要构建。

页面默认简体中文。右上角可以切到 English，两套文案说的是同一件事。

## 本地预览

在仓库根目录执行：

```bash
python3 -m http.server 8000
```

浏览器打开 http://localhost:8000

## 开启 GitHub Pages

1. 先把这个页面合并到 `main`。站点文件在仓库根目录，包含 `index.html` 和 `.nojekyll`。
2. 打开仓库的 **Settings → Pages**。
3. 在 **Build and deployment** 里，Source 选 **Deploy from a branch**。
4. Branch 选 **main**，文件夹选 **/ (root)**。
5. 保存。

生效后的地址：

https://upintheair6127.github.io/up-homepage/

第一次部署可能要等一两分钟。根目录的 `.nojekyll` 用来关掉 Jekyll，避免 GitHub 漏掉或改写静态文件。

## 需要补上的 TODO

未知的链接和联系方式没有编造，页面上标成「待补充」，源码里用 `data-todo` 和 HTML 注释标出。填的时候直接改 `index.html`。

| 标记 | 现在的样子 | 要填什么 |
| --- | --- | --- |
| `data-todo="link-xiaohongshu"` | `href="#"` | 小红书账号「Neal.」的主页链接 |
| `data-todo="link-wechat-channels"` | `href="#"` | 微信视频号「出海者Neal」的链接 |
| `data-todo="link-x"` | `href="#"` | X 主页链接 |
| `data-todo="handle-x"` | 文案「待补充账号」 | X 账号名。不知道就继续留着，不要编 |
| `data-todo="link-youtube"` | `href="#"` | YouTube 频道链接 |
| `data-todo="handle-youtube"` | 文案「待补充账号」 | YouTube 频道名。不知道就继续留着，不要编 |
| `data-todo="contact-method"` | 联系区的虚线框 | 联系方式（邮箱或其他）。不要写真实姓名 |

这 7 处都在 `index.html` 里，旁边有对应的 `<!-- TODO: ... -->` 注释。

## 填写时不要加的东西

- 真实姓名、真人照片
- 雇主名称
- 咖啡馆的具体店名（咖啡馆只写 2016 年起、在澳大利亚）
- 粉丝数、营业额、客户名单，以及其他没有出处的数字

经历里只有两个年份：2016（澳洲开咖啡馆）和 2026（AI 实践）。不要给中间两段另编年份。

## 文件

- `index.html` — 页面
- `css/styles.css` — 样式
- `js/main.js` — 打字、关键词轮换、滚动显现、时间线、进度条、中英文切换
- `favicon.svg` — 图标（几何图形，不是照片）
- `.nojekyll` — 让 GitHub Pages 不要走 Jekyll
