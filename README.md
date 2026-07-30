# Climate-Resilient Structures — Special Issue CFP (Static Site)

Structures (Elsevier) 特刊征稿网页。纯静态单页，零依赖、零构建。

## 目录结构

```
web/
├── index.html              # 单文件页面（内联 CSS/JS，含 EN/FR/ZH 三语）
├── .nojekyll               # 跳过 Jekyll 处理（Gitee/GitHub Pages 通用）
├── cfp_qr.png              # 二维码（指向当前部署地址，换域名后需重生成）
├── social_copy.md          # LinkedIn / 朋友圈 文案 + 发布方式
└── assets/
    ├── cfp-social-card.png          # LinkedIn 配图（横版 1.91:1，无二维码）
    ├── cfp-social-card-wechat.png   # 朋友圈配图（右下角含二维码）
    ├── you-dong.jpg
    ├── emilio-bastidas-arteaga.jpg
    ├── hongyuan-guo.jpg
    └── baixi-chen.jpg
```

## 部署到 Gitee Pages

> 前提：Gitee 账号 `hyguo93` 已完成**实名认证**，且「Gitee Pages」服务对个人开放（登录后在仓库「服务」菜单确认）。

1. 在 Gitee 新建**公开**仓库，建议名 `structures-cfp`。
2. 把本目录（`web/` 内所有文件）推到仓库根目录（含 `index.html` 与 `.nojekyll`）。

   ```bash
   cd web
   git init
   git add .
   git commit -m "CFP site"
   git remote add origin https://gitee.com/hyguo93/structures-cfp.git
   git push -u origin main
   ```

   > 若默认分支是 `master`，把上面 `main` 换成 `master`。
3. 仓库页 → **服务** → **Gitee Pages** → 部署分支选 `main`/`master`，部署目录选 **`/`**（根目录）→ 点击「启动 / 部署」。
4. 部署完成后访问：`https://hyguo93.gitee.io/structures-cfp/`
5. 以后更新内容，重新 `git push` 后到 Gitee Pages 页面点 **「更新」** 才会生效。

### 换域名后的连锁更新

Gitee 地址与临时沙箱不同，以下需重做（可让 WorkBuddy 执行）：

- `cfp_qr.png`（二维码指向新地址）
- `assets/cfp-social-card-wechat.png`（重叠新二维码）
- `social_copy.md` 中的「当前 H5」链接
- `og:image` 已用相对路径 `assets/cfp-social-card.png`，**无需改**，会自动解析为新域名。

## 本地预览

```bash
cd web && python -m http.server 8080
# 浏览器打开 http://localhost:8080
```

## 注意

- 页面语言按浏览器语言自动检测（回退英文），可手动切换 EN/FR/中文，选择记在 localStorage。
- 法文术语：UHPC→BTHP、FRP→PRF、mass timber→bois massif；英文技术词保留以利检索。
- 编辑信息以已上线网页为准（Baixi Chen 单位 UCF）。
