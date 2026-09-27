# DeepSeek Color — DSH 皮肤包

把 **DeepSeek Color** 五大色卡带进 DeepSeek Harness 桌面端 / Web UI。
纯 token 皮肤（L1，只重映射官方 `--dsw-alias-*` 语义 token），零补丁、零脚本、零背景媒体——最安全的一类皮肤。

![DeepSeek Color 五大色卡](docs/share-poster.png)

## 演示

▶️ [观看 20 秒演示视频](docs/demo.mp4)——五套皮肤切换效果一览（GitHub 文件页内可直接播放）。

## 五套皮肤

| 皮肤 | 目录 | 基调 | 适用场景 |
|---|---|---|---|
| 深潜蓝 Deep Dive Blue | `skins/deep-dive-blue` | 冷白纸底 × 深潜蓝 `#4D6BFE` | AI 产品与官网（DeepSeek 主色系） |
| 鲸鱼浅青 Whale Cyan | `skins/whale-cyan` | 海盐底 × 鲸青 `#00B3F4` | 数据产品与开发者工具 |
| 深夜机房 Midnight Cluster | `skins/midnight-cluster` | 深海军蓝夜底 × 信号蓝 `#5B8CFF` | 暗色大屏与硬件发布 |
| 雾灰银 Silver Mist | `skins/silver-mist` | 中性灰银 × 深潜蓝 `#4D6BFE` | 金融与企业官网（最克制） |
| 珊瑚信号 Coral Signal | `skins/coral-signal` | 暖沙底 × 珊瑚橙 `#FF5A3C` | 消费级 AI 与内容产品 |

## 安装

前置：先装皮肤中心（皮肤系统的唯一加载器）：

```bash
dsh plugin --profile web add @linxin666/dsh-client-ui-skin-center@latest
```

然后把想要的皮肤目录拷进 `$DSH_HOME/skins/`（默认 `~/.dsh/skins/`）：

```bash
git clone https://github.com/78tyih/dsh-deepseek-color.git
mkdir -p ~/.dsh/skins
cp -r dsh-deepseek-color/skins/deep-dive-blue ~/.dsh/skins/   # 想要哪套拷哪套
```

重启 `dsh web`，进入 **设置 → 插件 → 皮肤中心**，点刷新后即可看到并试穿 / 应用。

## 设计说明

每套皮肤只改动设计 token，不碰 DOM、不带 JS：

- ** surfaces / borders / labels**：基底、发丝线边框、四级文字灰阶全部取自对应色卡
- **brand / interactive / buttons**：唯一的高对比强调色，只出现在品牌与主按钮
- **theme-agnostic**：色卡本身就是完整观感，值写在 `:root`，明暗模式下一致呈现

设计系统完整文档（10 个网页骨架、token 表、换肤工作流）见主仓库：
[78tyih/deepseek-color](https://github.com/78tyih/deepseek-color)

## License

MIT
