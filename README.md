# Uzbekistan Market Analysis · GitHub Pages

乌兹别克斯坦汽车平行进口市场分析的静态展示站，绑定自定义域名 `uzbekistan.used-car.cn`。

## 页面

| 路径 | 内容 |
| --- | --- |
| `/` | 门户首页 |
| `/report.html` | 完整分析报告（四维度验证、趋势图、行动建议、来源清单） |
| `/dashboard.html` | Top200 客户交互看板（搜索 / 筛选 / 排序 / 导出 CSV） |
| `/methodology.html` | B2B 决策人线索挖掘方法精要（4 页，独立访问地址，首页 03 号卡片入口） |

三份页面均为自包含 HTML：图表由内联 SVG 脚本绘制，数据内联注入，不依赖任何 CDN，离线可用；`methodology.html` 为自包含单页文档，支持浏览器打印为 A4 PDF。

**固定独立地址**：`https://uzbekistan.used-car.cn/methodology.html`（备用 `https://iguoxing.github.io/uzbekistan-used-car/methodology.html`）。后续更新站点其他页面不会改动此路径；源稿位于 `2026-11-14-08-04-47/乌兹别克斯坦B2B决策人挖掘_方法论手册.html`，更新时覆盖本文件即可。

## 部署

- Pages source：`main` 分支根目录
- 自定义域名：`uzbekistan.used-car.cn`（见 `CNAME`）
- DNS 要求：在 DNSPod 为 `used-car.cn` 增加 `uzbekistan` 的 CNAME 记录，指向 `iguoxing.github.io`
- `.nojekyll` 用于跳过 Jekyll 构建；`robots.txt` 禁止搜索引擎收录（页面含客户线索数据）

## 数据口径

- 汇总表：1,000 家进口商 / $686,243,307 / 35,156 票
- 明细表：5,000 行样本 / $116,598,162 / 906 票去重报关单，覆盖全量金额 17.0%，仅代表样本趋势
- HS 8703 中约 48% 为电动三轮车、滑板车与 SKD 散件，不等于乘用车整车
- 抱怨 / 搜索 / RFQ 三个维度在海关数据中无字段，报告证据来自公开检索

## 本地更新

```bash
git add . && git commit -m "update" && git push origin main
```

推送后 GitHub Pages 会自动重新构建。原始数据与客户打分模型见工作区 `build_uz.py` / `render_html.py`。

---
Eastar Motors · Market Intelligence · 2026-11-13
