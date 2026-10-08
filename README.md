# Pro Max 全球价格观察

ChatGPT Pro Max 月度配置价格的历史快照，按快照汇率换算为人民币参考值，默认显示不含税口径。

[在线查看价格快照](https://majiayu000.github.io/chatgpt-pro-max-pricing/)（2026-09-26，独立整理，非实时官方报价）。

- 232 个国家／地区的配置，39 种币种。
- 226 个地区可以计算税前价，6 个因缺少税前金额及税率保持留空。
- 支持地区搜索、币种和数据依据筛选、排序、来源详情及 CSV 导出。
- 支持“原价 / 不含税”切换，默认不含税；原价的含税状态按地区标注，排序、详情和导出同步切换。
- 可选最多 4 个地区并排对比当前视图的快照人民币参考值、原币原价及税前金额；缺少税前数据时保持“待核实”。
- “分享当前视图”链接保留搜索、筛选、排序、税费口径、页码和已选对比地区。
- 桌面与手机布局。
- 存储说明列出官方 Library 套餐额度、文件存储与模型上下文的区别，并提供官方文档链接和核对日期。

## 数据口径

价格来自 ChatGPT 公开定价配置接口，例如：

https://chatgpt.com/backend-anon/checkout_pricing_config/configs/US

价格快照为 2026-09-26。优先使用接口标记为 exclusive 的原价或支付服务商税前覆盖金额；只有含税价的条目按接口税率计算。配置存在不代表已经开放购买。

汇率由 [ExchangeRate-API](https://www.exchangerate-api.com) 提供，更新时间为 2026-09-26 00:02:32 UTC。人民币数值是快照参考换算，不是官方人民币售价或当前结账报价。“不含税”模式展示税前金额；“原价”模式沿用各地区的含税或未含税标记，含税原价的人民币换算值也包含相应税额。两种模式均未计银行卡汇差与手续费。App 内购价格另算。

这是静态快照，不自动刷新。每行详情保留对应的官方配置来源。

## 查看、比较与分享

在[价格表](https://majiayu000.github.io/chatgpt-pro-max-pricing/#prices)搜索地区名称或代码，切换原价/不含税，再打开详情核对来源。最多选择四个地区对比；分享链接保留当前筛选和口径，CSV 导出当前结果。页面中的[使用说明与常见问题](https://majiayu000.github.io/chatgpt-pro-max-pricing/#pricing-help)解释参考换算、购买可用性与网页/App 差异。

当前权益和购买价格请查 [ChatGPT 官方套餐页](https://chatgpt.com/pricing/)及 [OpenAI 多币种账单说明](https://help.openai.com/en/articles/10421635-multi-currency-billing-faq)。数据问题请在[本项目 Issues](https://github.com/majiayu000/chatgpt-pro-max-pricing/issues)提供国家代码与公开来源。

## 本地预览

直接打开 `index.html`，或运行：

```sh
python3 -m http.server 8877
```

页面数据、样式和交互脚本已内嵌。Geist、Geist Mono 和 Noto Sans SC 字体通过 Google Fonts 非阻塞加载；加载较慢或不可用时使用现有本地字体回退。

## 发布

GitHub Pages 从 `codex/publish` 分支的根目录发布。

独立数据整理，非 OpenAI 官方网站。UI 参考本地 model-chronicle 项目。
