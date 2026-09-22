# 雾屿 · 图片仓库

博客 <https://railgun.ltd> 用的配图都放在这里，和博客源码分开，方便复用和替换。

| 字段 | 说明 |
|---|---|
| 用途 | 博客图集、文章封面 |
| 文件命名 | 小写下划线，语义化，例如 `fog-river-autumn.jpg` |
| 建议规格 | 长边 1400px、单张 ≤300KB 的 JPEG |
| 现有图片 | 21 张，合计 4.9 MB |

## 怎么引用

仓库开启 GitHub Pages 后（分支 `main`、根目录），图片地址是：

```
https://railgun.ltd/img/<文件名>.jpg
```

也可以用 jsDelivr 的免费 CDN（同一个仓库，不用额外配置，缓存更激进）：

```
https://cdn.jsdelivr.net/gh/1099298297/img@main/<文件名>.jpg
```

博客那边只要改 `content/site.json` 里的 `imgBase` 就能在两种地址（以及本地 `assets/img/`）之间切换。

## 加新图

```powershell
git add 新照片.jpg
git commit -m "add: 新照片"
git push
```

推完等 1~2 分钟就能访问。新图记得在博客的 `content/gallery/` 里加一条对应的 `.md`，
并把作者 / 许可写进去（如果是别人的图）。

## 版权

仓库里的图片**不是同一批人拍的**，作者与许可见 [CREDITS.md](CREDITS.md)。
这些图都是自由版权（CC / 公有领域），但**署名要求会跟着图片走**——
转载或复用到别处时，请一并保留 CREDITS.md 里的作者信息。
