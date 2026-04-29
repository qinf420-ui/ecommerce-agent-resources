# ecommerce-agent-resources

本目录汇集**电商 × AI Agent**方向的调研与速查资料，面向正在为导购、运营、建站或 MCP/Skill 选型的产品与工程同学。内容与仓库代码解耦：此处为可读文档；本仓库上一级若包含业务侧导购 Skill（例如 `.claude/skills/shopping_assistant/`），可作为「落地实现」的补充参考。

---

## 包含内容

| 文件 | 说明 |
|---|---|
| **[ecommerce-skill-research.md](./ecommerce-skill-research.md)** | **电商领域 Skill / MCP / 协议调研报告**（调研时间标注于文内）：按 Shopify、Magento、WooCommerce 等平台与用途分类罗列公开 Skill；整理店铺数据读写、支付、采集、客服等方向的 MCP Server；并整理 UCP、ACP、AP2、A2A、MPP、WebMCP 等与 Agent Commerce 相关的协议及与社区的 skill 映射。文末附有来源仓库索引表。 |
| **[ecommerce-cli-tools.md](./ecommerce-cli-tools.md)** | **电商相关 CLI 工具全览**：覆盖电商平台 CLI（Shopify CLI、Stencil、WP-CLI / WC-CLI、Magento 等）、支付（Stripe CLI）、搜索与 CMS（Algolia、Contentful）、基础设施与部署（Vercel、Netlify、Firebase 等），含快速选型思路与面向用户说明。 |

---

## 使用建议

- **选型或扫盲**：先看 `ecommerce-skill-research.md` 的目录与附录来源索引，再按需深入某一节。
- **落地开发**：结合目标平台官方文档与各 Skill 指向的 Repo；CLI 操作流程可参考 `ecommerce-cli-tools.md`。
- **数据时效**：调研文中的仓库版本、协议链接以文档内日期与原文为准；公开仓库会迭代，使用前建议核对上游 README/SKILL。

---
## 说明
- 调研均由 Claude Code完成
---


## 许可

本项目文档与附属文件遵循 [LICENSE](./LICENSE) 中的条款。
