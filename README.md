# Pro Max 全球价格观察

ChatGPT Pro Max 月度配置价格，统一换算为人民币税前金额。

- 232 个国家／地区的配置，39 种币种。
- 226 个地区可以计算税前价，6 个因缺少税前金额及税率保持留空。
- 支持地区搜索、币种和数据依据筛选、排序、来源详情及 CSV 导出。
- 支持“原价 / 不含税”切换，默认不含税；原价的含税状态按地区标注，排序、详情和导出同步切换。
- 桌面与手机布局。
- 存储说明列出官方 Library 套餐额度、文件存储与模型上下文的区别，并提供官方文档链接和核对日期。

## 数据口径

价格来自 ChatGPT 公开定价配置接口，例如：

https://chatgpt.com/backend-anon/checkout_pricing_config/configs/US

价格快照为 2026-09-26。优先使用接口标记为 exclusive 的原价或支付服务商税前覆盖金额；只有含税价的条目按接口税率计算。配置存在不代表已经开放购买。

汇率由 [ExchangeRate-API](https://www.exchangerate-api.com) 提供，更新时间为 2026-09-26 00:02:32 UTC。人民币数值是参考换算，不是官方人民币售价，不含税费、银行卡汇差与手续费。App 内购价格另算。

这是静态快照，不自动刷新。每行详情保留对应的官方配置来源。

## 本地预览

直接打开 `index.html`，或运行：

```sh
python3 -m http.server 8877
```

页面数据、样式和交互脚本已内嵌。Geist、Geist Mono 和 Noto Sans SC 字体通过 Google Fonts 加载，不可用时使用本地字体。

## 发布

GitHub Pages 从 `codex/publish` 分支的根目录发布。

独立数据整理，非 OpenAI 官方网站。UI 参考本地 model-chronicle 项目。
