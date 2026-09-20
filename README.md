# 学术主页（GitHub Pages）

基于个人简历生成的学术主页，单文件 `index.html`（无构建依赖、无外部库），中英双语切换，开箱即用。

## 部署到 GitHub Pages（5 分钟）

### 方式一：`username.github.io` 主站（推荐）

1. 在 GitHub 新建仓库，仓库名必须是 **`<你的用户名>.github.io`**（Public）。
2. 在本目录执行：

   ```bash
   git init
   git add .
   git commit -m "Initial academic homepage"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/<你的用户名>.github.io.git
   git push -u origin main
   ```

3. 等待 1–2 分钟，访问 `https://<你的用户名>.github.io` 即可。

### 方式二：项目页（`username.github.io/repo`）

1. 新建任意名称的 Public 仓库（如 `homepage`），推送本目录内容。
2. 仓库页面 → **Settings → Pages → Source** 选择 `main` 分支 `/ (root)` → Save。
3. 访问 `https://<你的用户名>.github.io/homepage/`。

> 本目录已执行过 `git init` 和首次提交，可直接添加远程仓库后 `git push`。

## 上线前需要替换的内容

在 `index.html` 中搜索以下标记并修改：

| 位置 | 说明 |
|---|---|
| `Google Scholar` / `ORCID` / `GitHub` 链接（`href="#"`） | 替换为你的真实主页链接 |
| `div.avatar` | 替换为真实照片：`<img src="avatar.jpg" style="width:128px;height:128px;border-radius:50%;object-fit:cover">`，并把照片文件放入本目录 |
| 页脚年份 / News 板块 | 后续有新动态时在 News 区域顶部追加即可 |

## 自定义域名（可选）

1. 在仓库根目录新建 `CNAME` 文件，内容为 `www.yourdomain.com`。
2. 在你的 DNS 服务商处添加 CNAME 记录指向 `<你的用户名>.github.io`。
