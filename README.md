# 雾屿 · 图片仓库

博客 <https://railgun.ltd> 用的图都放这里，和博客源码分开，方便复用和替换。

## 目录约定

| 目录 | 放什么 | 会不会出现在博客图集里 |
|---|---|---|
| `photos/` | 你想在图集里展示的照片（风景、生活…） | **会** —— 前提是在 `content/gallery/` 里写了对应条目 |
| `posts/` | 文章配图：代码截图、示意图、流程图、报错截图… | **不会**，只在正文里用 `![说明](posts/xxx.png)` 引用 |

现在 `photos/` 里是两类：博客图集现役的 13 张（自己拍的，见上一节）＋ 早先用过的 21 张自由版权照片
（已不进图集，`frost-morning.jpg` 还作文章封面）。谁是谁看 [CREDITS.md](CREDITS.md)。

**图集只认博客仓库里 `content/gallery/*.md` 的条目**，一个 `.md` 一格。
图片仓库里放再多东西（哪怕几千张代码截图），只要不写图集条目，就永远不会出现在图集里。

## 引用地址

```
https://railgun.ltd/img/photos/fog-river-autumn.jpg                ← GitHub Pages
https://cdn.jsdelivr.net/gh/1099298297/img@main/photos/xxx.jpg     ← jsDelivr CDN（零配置）
```

博客里只写相对路径，构建时自动拼：

```markdown
img: photos/fog-river-autumn.jpg      # 图集条目
cover: photos/frost-morning.jpg       # 文章封面
![第 3 步的报错](posts/error-01.png)  # 正文插图，不进图集
```

## 加新图

```powershell
git add posts/新截图.png
git commit -m "add: 文章配图"
git push
```

推完 1~2 分钟生效。图集照片建议长边 1400px、单张 ≤300KB；代码截图可以直接放 PNG。

## 版权

图集照片由站主本人拍摄，保留所有权利；自由版权的旧图作者与许可见 [CREDITS.md](CREDITS.md)。
自由版权的署名要求跟着图片走，复用到别处时请一并保留。
