# 我不是夸父 I Am Not Kua Fu — 投稿网页与简历

为法国艺术展投稿准备的两个语言版本，网页与 PDF 版式一致。

## 文件

| 文件 | 说明 |
|---|---|
| `index.html` | 中文网页（单页滚动：项目、故事、世界、界面、团队、艺术家）。作品为 VR 沉浸式叙事游戏，延续《仙儿》的 VR 路线 |
| `en.html` | English site (same layout) |
| `cv-zh.pdf` | 中文 A4 文档，11 页 |
| `cv-en.pdf` | 英文 A4 文档，11 页 |
| `cv.html` / `cv-en.html` | 上述 PDF 的源文件（打印样式），修改后可直接重新导出 |
| `assets/` | 图片与样式表（`style.css` 网页用，`cv.css` 打印用） |

## PDF 页码

01 封面 · 02 项目 · 03 故事（四章 + 四种结局）· 04 世界与角色（含 MR 眼镜 / 夸父 / 共振 设定）· 05 界面与制作 · 06 团队 · 07 艺术家 · 08 代表作品 · 09 展览 · 10 电影节与获奖 · 11 联系

## 打开方式

- 网页：直接双击 `index.html`（或 `en.html`），无需服务器，离线可用。
- PDF：`cv-zh.pdf`、`cv-en.pdf` 可直接提交或打印。

## 网页上的两个细节

1. **中英切换**：右上角的胶囊开关，点一下换语言。
2. **隐藏彩蛋**：页脚右下角有一个小小的「直播模式 / Live mode」开关。打开后整站瞬间变成多巴胺配色的直播间——糖果渐变、粗黑描边、跑马灯横幅、贴纸标签、每张图都挂上价格牌，右下角还会出现「立即购买」。再点一次回到原来的深色画册风格。状态会记录在 localStorage 里。

## 重新导出 PDF

修改 `cv.html` 后，用 Edge 无头模式重新打印：

```powershell
& "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" `
  --headless --no-sandbox --disable-gpu --no-pdf-header-footer `
  --virtual-time-budget=8000 `
  --print-to-pdf="cv-zh.pdf" "file:///D:/VsCodeProject/Kuafu_Submission/cv.html"
```

把 `cv.html` 换成 `cv-en.html` 即可导出英文版。

## 内容来源

文字取自 `../Kuafu/` 中的原始资料：《周昉简介》《周昉简历》《〈轮回〉作品介绍》《Director's Statement》《〈仙儿〉作品信息》《〈直播间〉作品说明》，以及更新后的《故事设计》（章节结构、四种结局、MR 眼镜等设定）。图片取自同一文件夹的作品海报、剧照、角色三视图、故事板与 UI 设计稿。

## 版式约定

- 深色底 `#0b0a09`，朱红强调色 `#c4433a`（取自《轮回》海报的雾红与《直播间》的红裙）。
- 标题宋体、正文微软雅黑 Light；英文标题 Georgia。
- PDF 为 210×297mm 固定页面，每页内容在导出前已核对，无跨页断裂。
