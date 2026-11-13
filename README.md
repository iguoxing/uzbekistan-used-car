# Uzbekistan Market Analysis · GitHub Pages

乌兹别克斯坦汽车平行进口市场分析的静态展示站，绑定自定义域名 `uzbekistan.used-car.cn`。

## 页面

| 路径 | 内容 |
| --- | --- |
| `/` | 门户首页 |
| `/report.html` | 完整分析报告（四维度验证、趋势图、行动建议、来源清单） |
| `/dashboard.html` | Top200 客户交互看板（搜索 / 筛选 / 排序 / 导出 CSV） |

两份页面均为自包含 HTML：图表由内联 SVG 脚本绘制，数据内联注入，不依赖任何 CDN，离线可用。

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
