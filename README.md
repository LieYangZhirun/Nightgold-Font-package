# Nightgold Font Package

主题"黑夜与金"专用字体集合，通过 jsDelivr CDN 自托管以保证可用性与加载速度。

## 字体清单

| 字体家族 | 用途 | 字重 | 文件大小 |
|---------|------|------|---------|
| **Inter** | UI / 控件 / 正文（西文） | 400 / 500 / 700 | ~419 KB（3 个文件） |
| **Source Han Sans SC** | UI / 控件 / 正文（中文回退） | 400 / 500 / 700 | ~23.5 MB（3 个文件） |
| **JetBrains Mono** | 代码块 / 编辑器（西文） | 400 / 500 / 700 | ~274 KB（3 个文件） |
| **LXGW WenKai** | 文学化渲染（引用块、推理标题） | 400 | ~6.5 MB |
| **LXGW WenKai Mono** | 代码 CJK 等宽回退 | 400 | ~6.5 MB |

**总计：** ~37.2 MB（11 个 woff2 文件）

### 字体特性

- **Inter**：现代几何无衬线字体，专为屏幕显示优化，支持 OpenType 特性
- **Source Han Sans SC**：Adobe 与 Google 联合开发的思源黑体简体中文版，覆盖完整 CJK 字符集
- **JetBrains Mono**：专为开发者设计的等宽字体，具有清晰的字符区分度（0/O, 1/l/I）
- **LXGW WenKai**：基于 Klee One 的开源中文楷体，兼具传统书法韵味与现代可读性
- **LXGW WenKai Mono**：霞鹜文楷的等宽版本，适用于代码中的中文注释

### Unicode 范围限制

Inter 和 JetBrains Mono 已配置 `unicode-range` 白名单（U+0020-007E, U+00A0-00FF, U+0100-017F），仅覆盖西文常用字符（拉丁字母、数字、基本标点及扩展拉丁字符）。其他字符（如弯引号、破折号、CJK 标点等）会自动回退到字体栈中的中文字体，确保中英混排的视觉一致性。

## 使用方法

### 在 CSS 中引入

```css
@import url('https://cdn.jsdelivr.net/gh/LieYangZhirun/Nightgold-Font-package@main/fonts.css');
```

### 字体栈配置示例

```css
:root {
    /* 无衬线字体栈（UI / 正文） */
    --font-sans: 'Inter', 'Source Han Sans SC', sans-serif;
    
    /* 楷体字体栈（文学化渲染） */
    --font-serif: 'LXGW WenKai', 'KaiTi', 'STKaiti', serif;
    
    /* 等宽字体栈（代码块） */
    --font-mono: 'JetBrains Mono', 'LXGW WenKai Mono', monospace;
}
```

### jsDelivr CDN 说明

- **自动缓存**：jsDelivr 会自动缓存 GitHub 仓库内容，全球 CDN 加速
- **版本控制**：
  - `@main` - 始终指向最新主分支（推荐用于开发）
  - `@1.0.0` - 指定 tag 版本（推荐用于生产环境）
  - `@commit-hash` - 指定具体 commit
- **强制刷新**：如需清除 CDN 缓存，可在 URL 后添加 `?v=timestamp`

## 文件结构

```
Nightgold-Font-package/
├── fonts/
│   ├── inter/
│   │   ├── Inter-Regular.woff2      (138 KB)
│   │   ├── Inter-Medium.woff2       (140 KB)
│   │   └── Inter-Bold.woff2         (141 KB)
│   ├── source-han-sans-sc/
│   │   ├── SourceHanSansSC-Regular.woff2  (7.7 MB)
│   │   ├── SourceHanSansSC-Medium.woff2   (7.9 MB)
│   │   └── SourceHanSansSC-Bold.woff2     (8.2 MB)
│   ├── jetbrains-mono/
│   │   ├── JetBrainsMono-Regular.woff2    (90 KB)
│   │   ├── JetBrainsMono-Medium.woff2     (92 KB)
│   │   └── JetBrainsMono-Bold.woff2       (92 KB)
│   ├── lxgw-wenkai/
│   │   └── LXGWWenKai-Regular.woff2       (6.5 MB)
│   └── lxgw-wenkai-mono/
│       └── LXGWWenKaiMono-Regular.woff2   (6.5 MB)
├── fonts.css          # 字体声明文件
├── LICENSE            # MIT 许可证
└── README.md          # 本文件
```

## 许可证

本仓库采用 **MIT License** 许可（见 [LICENSE](LICENSE) 文件）。

所包含的字体均为开源字体，遵循各自的原始许可证：

| 字体 | 许可证 | 来源 |
|------|--------|------|
| Inter | [SIL Open Font License 1.1](https://github.com/rsms/inter/blob/master/LICENSE.txt) | [rsms/inter](https://github.com/rsms/inter) |
| Source Han Sans SC | [SIL Open Font License 1.1](https://github.com/adobe-fonts/source-han-sans/blob/master/LICENSE.txt) | [adobe-fonts/source-han-sans](https://github.com/adobe-fonts/source-han-sans) |
| JetBrains Mono | [SIL Open Font License 1.1](https://github.com/JetBrains/JetBrainsMono/blob/master/OFL.txt) | [JetBrains/JetBrainsMono](https://github.com/JetBrains/JetBrainsMono) |
| LXGW WenKai | [SIL Open Font License 1.1](https://github.com/lxgw/LxgwWenKai/blob/main/SIL_Open_Font_License_1.1.txt) | [lxgw/LxgwWenKai](https://github.com/lxgw/LxgwWenKai) |
| LXGW WenKai Mono | [SIL Open Font License 1.1](https://github.com/lxgw/LxgwWenKai/blob/main/SIL_Open_Font_License_1.1.txt) | [lxgw/LxgwWenKai](https://github.com/lxgw/LxgwWenKai) |

**SIL OFL 1.1 许可证要点：**
- ✅ 可自由使用、修改、分发
- ✅ 可用于商业项目
- ✅ 可嵌入到软件或网站中
- ❌ 不可单独出售字体文件本身
- ❌ 修改后的字体不可使用原字体的保留名称
