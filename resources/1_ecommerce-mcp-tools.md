# 电商领域 MCP Server 全览

> **调研时间**：2026 年 4 月
> **数据来源**：逐一 fetch 各 GitHub repo 的 README 及官方文档
> **说明**：MCP Server 是实时 API 连接层，让 AI Agent 通过自然语言直接执行店铺操作。与 Skill（指令包）不同，MCP 需要 API 凭证才能访问真实数据。

---

## 目录

| 分类 | MCP 数量 | 主要用户 |
|------|---------|---------|
| [店铺数据读写（国际平台）](#店铺数据读写国际平台) | 3 个 | 商家、开发者（后端）、AI（商家侧） |
| [店铺数据读写（国内平台）](#店铺数据读写国内平台) | 1 个 | 消费者、AI（消费者侧） |
| [支付操作](#支付操作) | 1 个 | 商家、开发者（后端）、AI（商家侧） |
| [数据采集](#数据采集) | 1 个 | 商家、开发者（后端）、AI（商家侧） |
| [客服自动化](#客服自动化) | 1 个 | 商家、AI（商家侧） |

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

## 店铺数据读写（国际平台）

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 面向用户 |
|----------|-------------|------|---------------|----------|----------|
| `shopify-mcp` | [GeLi2001/shopify-mcp](https://github.com/GeLi2001/shopify-mcp)<br>npm: `shopify-mcp` | 最活跃的 Shopify MCP，基于 GraphQL Admin API 2026-01，AI 可直接查询和操作店铺数据 | 产品管理 8 个工具（CRUD 产品/变体/选项）；客户管理 8 个工具（CRUD/合并/地址）；订单管理 10 个工具（查询/取消/关闭/标记已付款/履行/退款）；Metafield 管理 3 个工具；库存管理 1 个工具；标签管理 1 个工具 | Shopify | 🏪 商家<br>🤖 AI（商家侧）<br>🔧 开发者（后端） |
| `Shopify Dev MCP` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit)<br>npm: `@shopify/dev-mcp`（官方） | Shopify 官方开发文档 MCP，实时搜索 shopify.dev 文档，不直接操作店铺数据 | shopify.dev 全站文档搜索；API 字段/schema/示例代码查询；API 版本与废弃字段确认 | Shopify | 🔧 开发者（后端） |
| `shopify-admin` | [askphill/ww](https://github.com/askphill/ww/blob/main/.claude/skills/shopify-admin/SKILL.md) | shell 脚本封装的轻量级 Shopify Admin 操作，专注媒体资产管理 | 产品查询（搜索/分页）；文件/图片/视频查询；媒体文件上传（jpg/png/gif/webp/svg/mp4/mov/pdf） | Shopify | 🏪 商家<br>🤖 AI（商家侧） |

---

## 店铺数据读写（国内平台）

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 面向用户 |
|----------|-------------|------|---------------|----------|----------|
| `taobao-native MCP` | 淘宝桌面版 v2.5.0（内置）<br>[jianghu.taobao.com](https://jianghu.taobao.com/detail/47301_68957160) | 通过淘宝桌面客户端暴露的本地 MCP 服务，让 AI 智能体直接操控已登录的淘宝客户端完成购物全流程。MCP 地址：localhost:3654/mcp | search_products（商品搜索/比价）；get_product_detail/get_product_skus（商品详情/规格）；add_to_cart（加购）；navigate_to_page（首页/购物车/订单/天猫）；订单查询/催发货/开发票；read_page_content/scan_page_elements（页面读取） | 淘宝 / 天猫 | 👤 消费者<br>🤖 AI（消费者侧） |

---

## 支付操作

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 面向用户 |
|----------|-------------|------|---------------|----------|----------|
| `Stripe MCP` | [Stripe 官方 MCP Registry](https://github.com/mcp)<br>Claude.ai 可直接连接 | Stripe 官方 MCP，覆盖客户、产品、支付、退款和订阅的完整管理 | 客户查询与创建；产品/价格管理；PaymentIntent 状态查询；退款处理；订阅管理；Webhook 端点管理 | 通用 | 🏪 商家<br>🤖 AI（商家侧）<br>🔧 开发者（后端） |

---

## 数据采集

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 面向用户 |
|----------|-------------|------|---------------|----------|----------|
| `Apify MCP` | [apify/apify-mcp-server](https://github.com/apify/apify-mcp-server)<br>URL: `https://mcp.apify.com`（支持 OAuth） | 8000+ Actors 的数据采集 MCP，覆盖主流电商平台的产品、评论、价格数据抓取 | 亚马逊产品/评论/搜索数据爬取；竞品价格监控；社交电商数据（TikTok Shop/Instagram）；Google Shopping 数据抓取；8000+ 专项 Actor 按需调用 | 通用（多平台） | 🏪 商家<br>🤖 AI（商家侧）<br>🔧 开发者（后端） |

---

## 客服自动化

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 面向用户 |
|----------|-------------|------|---------------|----------|----------|
| `Enneagora MCP` | [slavpilus/mcp](https://github.com/slavpilus/mcp) | 平台无关的电商客服 MCP，14 个工具覆盖从订单查询到售后政策的完整客服场景 | 订单查询/追踪/状态更新（4 个工具）；退货政策/配送信息/联系方式问答（4 个工具）；尺码指南/保修/产品护理信息（3 个工具）；支付方式/账户帮助/积分计划（3 个工具） | 通用（Shopify/Magento 策略层规划中） | 🏪 商家<br>🤖 AI（商家侧） |

---

## MCP Server 来源索引

| Repo | MCP 工具数量 | 许可证 |
|------|-------------|--------|
| [GeLi2001/shopify-mcp](https://github.com/GeLi2001/shopify-mcp) | 31 个工具 | — |
| [apify/apify-mcp-server](https://github.com/apify/apify-mcp-server) | 8000+ Actors | Apache 2.0 |
| [slavpilus/mcp](https://github.com/slavpilus/mcp) | 14 个工具 | — |

---

*最后更新：2026 年 4 月 | 数据来源：各 GitHub repo README 及官方文档*
