# ecommerce-agent-resources

本目录汇集**电商 × AI Agent**方向的调研与速查资料，面向正在为导购、运营、建站或 MCP/Skill 选型的产品与工程同学。

---

## 项目结构

```
ecommerce-agent-resources/
├── ecommerce-cli-tools.md      # CLI 工具全览
├── ecommerce-skill-library.md # Skill 库全览
├── ecommerce-mcp-tools.md     # MCP Server 全览
└── ecommerce-protocol.md      # Agentic Commerce 协议全览
```

---

## 文件说明

| 文件 | 说明 |
|------|------|
| **ecommerce-cli-tools.md** | 电商相关 CLI 工具全览，覆盖平台 CLI（Shopify CLI、Stencil、WP-CLI、Magento 等）、支付（Stripe CLI）、搜索与 CMS（Algolia、Contentful）、部署（Vercel、Netlify、Firebase、AWS）等，含快速选型建议与面向用户标签。 |
| **ecommerce-skill-library.md** | 电商领域 Skill 库全览，按平台（Shopify、Magento、WooCommerce 等）与用途分类罗列公开 Skill，包含前端开发、后端开发、商品运营、消费者自动化、支付、搜索、内容管理、部署运维、数据分析、营销等方向。 |
| **ecommerce-mcp-tools.md** | 电商领域 MCP Server 全览，整理店铺数据读写、支付操作、数据采集、客服自动化等方向的 MCP Server，说明各 Server 支持的工具能力与适用场景。 |
| **ecommerce-protocol.md** | Agentic Commerce 协议全览，整理 UCP、ACP、AP2、A2A、MPP、WebMCP 等与 AI Agent 购物相关的技术标准规范及社区 Skill 映射。 |

---

## 面向用户标签

| 标签 | 说明 |
|------|------|
| 👤 **消费者** | 个人用户手动操作，完成搜索、比价、下单等购物行为 |
| 🤖 **AI（消费者侧）** | AI 智能体代替消费者自动购物，复用买家账号权限 |
| 🏪 **商家** | 店铺运营者手动操作，管理商品、订单、客户、营销 |
| 🤖 **AI（商家侧）** | AI 智能体代替商家自动化运营，复用卖家账号权限 |
| 🎨 **开发者（前端）** | 构建店铺展示层，开发主题、UI 组件、小程序前端 |
| 🔧 **开发者（后端）** | 构建店铺后台逻辑，开发插件、API 集成、部署运维 |

---

## 使用建议

- **选型或扫盲**：先看各文件的目录与来源索引，再按需深入某一节。
- **落地开发**：结合目标平台官方文档与各资源指向的 Repo。
- **数据时效**：调研文中的仓库版本、协议链接以文档内日期与原文为准；公开仓库会迭代，使用前建议核对上游 README/SKILL。

---

## 说明

- 调研由 Claude Code 完成

---

## 许可

本项目文档与附属文件遵循 [LICENSE](./LICENSE) 中的条款。
