# 📖 网站内容管理手册

> 所有操作都在 GitHub 网页上完成，不需要终端，不需要安装任何工具。
> 改完保存后，网站 1-2 分钟自动更新。

## 🌐 你的网站地址

- 中文：https://pinkyo3o.github.io/personal-website/zh/
- 英文：https://pinkyo3o.github.io/personal-website/en/
- GitHub 仓库：https://github.com/pinkyo3o/personal-website

---

## 📝 写新博客文章

### 中文文章

1. 打开 https://github.com/pinkyo3o/personal-website/tree/main/src/content/blog/zh
2. 点右上角 **Add file** → **Create new file**
3. 文件名填：`你的文章英文名.md`（比如 `my-first-post.md`）
4. 粘贴以下模板：

```
---
title: '这里是文章标题'
description: '这里是一句话摘要'
pubDate: 2026-08-25
tags: ['标签1', '标签2']
lang: 'zh'
---

这里写正文，用 Markdown 语法。

# 大标题
## 小标题

- 列表项1
- 列表项2

**加粗文字**

> 引用文字

[链接文字](网址)
```

5. 点绿色按钮 **Commit changes...** → 再点 **Commit changes**
6. 等 1-2 分钟，网站自动更新

### 英文文章

同上，但文件放在：
https://github.com/pinkyo3o/personal-website/tree/main/src/content/blog/en
模板里的 `lang: 'zh'` 改成 `lang: 'en'`

---

## ✏️ 编辑现有文章

1. 打开 https://github.com/pinkyo3o/personal-website
2. 依次点 `src` → `content` → `blog` → `zh`（或 `en`）
3. 点你要编辑的文章文件名
4. 点右上角 **铅笔图标** ✏️
5. 修改内容
6. 点 **Commit changes...** → **Commit changes**

---

## 🗑️ 删除文章

1. 打开文章文件
2. 点右上角 **垃圾桶图标** 🗑️（或铅笔旁边的更多选项）
3. 确认删除

---

## 👤 修改个人信息（名字、简介、社交链接）

1. 打开 https://github.com/pinkyo3o/personal-website/blob/main/src/data/site.ts
2. 点右上角 **铅笔图标** ✏️
3. 修改内容（保持引号和格式不变）：

```
name: {
  zh: '你的中文名字',        ← 改这里
  en: 'Your English Name',  ← 改这里
},

tagline: {
  zh: '一句话简介',          ← 改这里
  en: 'One line tagline',   ← 改这里
},

about: {
  zh: `关于我的详细介绍...`,   ← 改这里
  en: `About me...`,        ← 改这里
},

social: {
  github: 'https://github.com/yourusername',  ← 改这里
  email: 'mailto:your@email.com',            ← 改这里
  twitter: '',                                ← 不用就留空
  linkedin: '',                               ← 不用就留空
  instagram: '',                              ← 不用就留空
},
```

4. 点 **Commit changes...** → **Commit changes**

---

## 🚀 修改项目展示

1. 打开 https://github.com/pinkyo3o/personal-website/blob/main/src/data/projects.ts
2. 点右上角 **铅笔图标** ✏️
3. 添加/修改项目（复制一个 `{ ... }` 块，修改内容）：

```
{
  title: {
    zh: '项目中文名',
    en: 'Project English Name',
  },
  description: {
    zh: '中文描述',
    en: 'English description',
  },
  tags: ['标签1', '标签2'],
  image: '',           ← 图片地址，没有就留空
  link: 'https://...',  ← 项目链接
  featured: true,      ← true=首页展示，false=不展示
},
```

4. 点 **Commit changes...** → **Commit changes**

---

## 🎨 修改主题颜色

1. 打开 https://github.com/pinkyo3o/personal-website/blob/main/src/styles/global.css
2. 点右上角 **铅笔图标** ✏️
3. 修改顶部的颜色值：

```
--color-primary: #f9a8c9;      /* 粉色（主色） */
--color-accent: #8ecae6;       /* 蓝色（辅色） */
--color-warmwhite: #fefcfd;    /* 背景色 */
```

颜色代码查询：https://www.google.com/search?q=color+picker

4. 点 **Commit changes...** → **Commit changes**

---

## 📋 修改导航栏文字

1. 打开 https://github.com/pinkyo3o/personal-website/blob/main/src/i18n/ui.ts
2. 点右上角 **铅笔图标** ✏️
3. 修改 `zh:` 下面的文字

---

## ⏰ 修改后多久网站更新？

每次 Commit changes 后：
1. GitHub 自动开始构建（约 30 秒）
2. 部署完成（约 1-2 分钟）
3. 网站更新

查看部署进度：https://github.com/pinkyo3o/personal-website/actions
- 🟡 黄色 = 正在部署
- ✅ 绿色 = 部署完成

---

## 💡 常见问题

**Q: 改完网站没变化？**
A: 按 Command + Shift + R 强制刷新浏览器，或用无痕窗口打开。

**Q: 改错了怎么办？**
A: 在 GitHub 文件页面点 "History"，可以查看历史版本并恢复。

**Q: 不小心删了文件？**
A: 在 GitHub 仓库页面可以看到所有历史记录，随时可以恢复。
