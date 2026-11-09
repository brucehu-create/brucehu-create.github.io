# 部署到 GitHub Pages

这个文件夹里是炫酷版简历的 GitHub 版本：

| 文件 | 用途 |
| --- | --- |
| `index.html` | 页面本体（单文件，样式与脚本全部内联） |
| `avatar.jpg` | 头像，页面与社交预览卡片共用 |

---

## 一、用 GitHub Pages 发布（推荐：5 分钟）

1. 打开 <https://github.com/new>，新建一个仓库
   - 想用 `https://brucehu-create.github.io/` 这种短地址 → 仓库名填 **`brucehu-create.github.io`**
   - 想用 `https://brucehu-create.github.io/cv/` → 仓库名填 **`cv`** 之类
   - 选 Public（私有仓库的 Pages 要付费）
2. 把 `index.html` 和 `avatar.jpg` 传到仓库根目录（网页上传即可）
3. 仓库 → **Settings** → 左侧 **Pages** → Source 选 **Deploy from a branch** → Branch 选 `main` + `/ (root)` → Save
4. 等 1–2 分钟，刷新 Pages 页面，顶部会出现网址

**网址规则**

- 仓库名 = `brucehu-create.github.io` → `https://brucehu-create.github.io/`
- 其他仓库名 → `https://brucehu-create.github.io/<仓库名>/`

---

## 二、自己本地看效果

直接双击 `index.html` 就能在浏览器打开（`avatar.jpg` 要和它放在同一目录）。

---

## 三、两处要注意的地方

**1. 隐私**

- 这个页面**不含手机号**，只保留邮箱和 GitHub 链接。
- 已加 `<meta name="robots" content="noindex,nofollow">`，搜索引擎不会收录；希望被搜到就删掉这一行。
- 上一级目录里那五版简历仍然保留了手机号——那是本地文件、不对外，需要一起删的话告诉我。

**2. 右上角的「学术版 ↗」**

部署版本里我已经把它改成了跳转到你的 GitHub 主页（因为 `academic.html` 没一起部署）。

想让它指向本地那版学术简历，就把 `href` 改回 `academic.html`，并把 `academic.html` 一起上传（同样可用）。

---

## 四、可选：绑定自定义域名

如果有自己的域名（比如 `huxianggao.com`），在仓库 Settings → Pages → Custom domain 里填上，再按提示加 DNS 记录即可。国内访问 GitHub Pages 有时不稳定，若在意可以换成 Cloudflare Pages / Vercel 托管，直接把这两个文件拖上去就行。
