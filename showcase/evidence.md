# evidence.md · dsh-deepseek-color

事实清单。展示文案只能引用本文件能支撑的结论。

## 已验证（Observed）

| 事实 | 方式 | 日期 |
|---|---|---|
| 5 套皮肤目录结构一致：`skin.css + skin.json + preview/light.jpg + preview/dark.jpg` | GitHub API 实查 | 2026-10-03 |
| 5 份 skin.css 全部只含 `:root` token 重映射（`--dsw-alias-*` / `--dsw-specific-*` / `--dsw-shadow-*`），无 JS、无补丁、无媒体引用 | 逐文件实读 | 2026-10-03 |
| `docs/` 含 `demo.mp4` 与 `share-poster.png` | GitHub API 实查 | 2026-10-03 |
| `LICENSE` = MIT，位于仓库根目录 | GitHub API 实查 | 2026-10-03 |
| token 值与 README 描述的基调一致（深潜蓝 #4D6BFE / 鲸青 #00B3F4 / 信号蓝 #5B8CFF / 深潜蓝 / 珊瑚橙 #FF5A3C） | skin.css 实读比对 | 2026-10-03 |

## 自述未独立复核（Inferred · Self-reported）

| 声明 | 复核方式 |
|---|---|
| 皮肤中心（@linxin666/dsh-client-ui-skin-center）安装→试穿→应用全流程可用 | 需 DSH 环境实测 |
| demo.mp4 为 20 秒五套切换演示 | 文件存在已验证；内容未看（时长自述） |

## 未验证（Unknown）

无。展示页所用素材（demo.mp4 / preview JPG / share-poster.png）全部经 jsDelivr CDN 引用，发布时 curl 验证 200 + 正确 MIME。

## 授权边界

- MIT License——代码与 token 可自由复制、修改、再分发（保留版权声明）。
