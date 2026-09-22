# 如何自行修改学术主页

这个网站采用 GitHub Pages + Jekyll。日常更新不需要写代码，也不需要在电脑上安装软件。

## 最常用的修改方式

1. 打开仓库中的 [`_data/profile.yml`](./_data/profile.yml)。
2. 点击右上角的铅笔图标（Edit this file）。
3. 修改相应文字。请保留每一行开头的空格层级。
4. 页面底部点击 **Commit changes**。
5. 通常等待 1–3 分钟，网页会自动更新。

## 添加一篇论文

在 `publications:` 下复制一整段论文记录，粘贴到合适位置并修改内容：

```yaml
  - year: "2026"
    type: Journal article
    title: Your paper title
    authors: Author One, Jianfeng Ning and Author Three
    venue: Journal Name, volume, pages or article number
    url: https://doi.org/your-doi
```

注意事项：

- 年份建议加英文双引号，例如 `"2026"`。
- 冒号较多的标题建议整体加双引号。
- 每篇论文开头的 `-` 以及后续字段前的空格不要删除。
- `url` 建议使用出版社、DOI 或 arXiv 的永久链接。

## 添加经历或奖项

经历位于 `experience:`，奖项位于 `awards:`。复制现有项目再修改是最稳妥的方法。

## 更新头像或 CV

- 头像：上传新文件并替换 `assets/img/jianfeng-ning.jpg`。建议使用横向或近方形 JPG，文件名保持不变。
- CV：上传新文件并替换 `assets/files/Jianfeng-Ning-CV.pdf`。文件名保持不变，页面上的 CV 链接无需修改。

在 GitHub 中打开目标文件后，可使用 **Add file → Upload files** 上传同名文件并覆盖。

## 修改颜色或版式

网站样式集中在 `assets/css/style.scss`。页面结构位于 `_layouts/homepage.html`。如果只是更新履历和论文，不需要修改这两个文件。

## 修改后没有立即显示

先等待几分钟并刷新页面。如果仍未更新，请打开仓库的 **Actions** 页面，查看最近一次 GitHub Pages 构建是否成功。YAML 中的缩进或未配对引号是最常见的错误。
