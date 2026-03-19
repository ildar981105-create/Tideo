# FrameX Studio — 长期记忆

## 仓库策略（2026-03-12 确定）

| 项目 | 用途 |
|------|------|
| `framex-studio`（origin） | **主开发仓库**，所有改动都在这里进行 |
| `framex-app`（framex 远程） | **发布镜像 / 备份**，只接受从 studio 同步推送，不直接修改 |
| `av-saas` | **已冻结归档**，不做任何修改 |

### 推送流程
1. 所有代码修改在 `framex-studio` 进行
2. `git push origin main` — 推到 studio 源码仓库
3. `git push framex main` — 同步到 framex-app 发布站点（需要时可 `--force`）

### GitHub Pages
- studio：`https://ildar981105-create.github.io/framex-studio/`
- app（镜像）：`https://ildar981105-create.github.io/framex-app/`

## 版本策略

| 功能模块 | 最新版本 | 废弃版本 |
|---------|---------|---------|
| 视频译制 | `translate-v6.html` | v3, v4, v5 |
| 编辑器 | `editor-v2.html` | editor.html |

## 页面架构

| 页面 | 文件 |
|------|------|
| 主入口 | `app/create.html` |
| 视频译制 | `app/translate-v6.html` |
| 直播剪辑 | `app/livestream.html` |
| AI 生成 | `app/generate.html` |
| 素材管理 | `app/media.html` |
| 我的作品 | `app/result.html` |
