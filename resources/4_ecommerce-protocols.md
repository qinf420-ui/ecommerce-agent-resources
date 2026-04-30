# Agentic Commerce 协议全览

> **调研时间**：2026 年 4 月
> **数据来源**：各协议官网及 GitHub 文档
> **说明**：协议是技术标准规范，不是 Skill 也不是 MCP。它们定义 AI Agent 如何安全地代替人类完成商务交易的通信方式与授权机制。

---

## 目录

| 协议 | 主导方 | 解决问题 | 核心机制 | 面向用户 |
|------|--------|---------|---------|----------|
| [UCP](#ucp-universal-commerce-protocol) | Google、Shopify | 构建完整 Agent 购物旅程标准接口 | Product Search；Unified Checkout；Identity Linking；Order Management | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| [ACP](#acp-agentic-commerce-protocol) | OpenAI、Stripe | AI Agent 在对话界面直接完成购买 | Shared Payment Token；Agentic Checkout API | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| [AP2](#ap2-agent-payments-protocol) | Google | 无人值守场景的支付授权证明 | Intent Mandate；Cart Mandate；Payment Mandate | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| [A2A](#a2a-agent-to-agent-protocol) | Google（Linux Foundation） | 不同 Agent 之间发现能力、委托任务 | Agent Card；Task Lifecycle；Push Notifications | 🤖 AI（消费者侧）<br>🤖 AI（商家侧）<br>🔧 开发者（后端） |
| [MPP](#mpp-machine-payments-protocol) | Stripe、Tempo Labs | 机器对机器自动付款（HTTP 402） | Charge Intent；Session Intent；mppx SDK | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| [WebMCP](#webmcp-web-model-context-protocol) | Google、Microsoft、W3C | 网站无需后端改造即可被 AI Agent 感知 | navigator.modelContext；registerTool；HTML 属性注解 | 🤖 AI（消费者侧）<br>🎨 开发者（前端） |

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

## UCP（Universal Commerce Protocol）

| 属性 | 说明 |
|------|------|
| **主导方** | Google、Shopify，联合 Etsy/Wayfair/Target/Walmart |
| **官网** | [ucp.dev](https://ucp.dev) |
| **解决的问题** | 构建从商品发现到结账到订单追踪的完整 Agent 购物旅程标准接口，消除 N×M 定制集成问题 |
| **核心机制** | Product Search；Unified Checkout（动态定价/税务）；Identity Linking（OAuth 2.0）；Order Management Webhook |
| **面向用户** | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| **对应 Skill** | [OrcaQubits `ucp-agentic-commerce`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/ucp-agentic-commerce)（15 个 skill） |

---

## ACP（Agentic Commerce Protocol）

| 属性 | 说明 |
|------|------|
| **主导方** | OpenAI、Stripe |
| **官网** | [agenticcommerce.dev](https://agenticcommerce.dev) |
| **解决的问题** | 让 AI Agent 在对话界面直接完成购买，确保 Agent 不接触用户支付凭证（PCI 合规） |
| **核心机制** | Shared Payment Token（SPT）：一次性支付令牌；Agentic Checkout API：create/update/complete/cancel；Delegated Payment：Stripe 作为支付中间人 |
| **面向用户** | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| **对应 Skill** | [OrcaQubits `acp-agentic-commerce`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/acp-agentic-commerce)（15 个 skill） |

---

## AP2（Agent Payments Protocol）

| 属性 | 说明 |
|------|------|
| **主导方** | Google |
| **官网** | [ap2-protocol.org](https://ap2-protocol.org) |
| **解决的问题** | 当 AI Agent 自主购物时，提供可加密验证的"用户已授权"证明，解决无人值守场景的支付纠纷 |
| **核心机制** | Intent Mandate（预授权）；Cart Mandate（特定购物车明确授权，用户签名不可抵赖）；Payment Mandate（支付网络风险评估信号）；所有 Mandate 均使用加密签名 |
| **面向用户** | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| **对应 Skill** | [OrcaQubits `ap2-agentic-payments`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/ap2-agentic-payments)（18 个 skill） |

---

## A2A（Agent-to-Agent Protocol）

| 属性 | 说明 |
|------|------|
| **主导方** | Google（现 Linux Foundation 维护） |
| **官网** | [a2a-protocol.org](https://a2a-protocol.org) |
| **解决的问题** | 不同公司、不同框架构建的 AI Agent 之间如何互相发现能力、委托任务和传递上下文 |
| **核心机制** | Agent Card（能力声明）；Task Lifecycle（任务状态机）；JSON-RPC Transport；Push Notifications（异步任务通知） |
| **面向用户** | 🤖 AI（消费者侧）<br>🤖 AI（商家侧）<br>🔧 开发者（后端） |
| **对应 Skill** | [OrcaQubits `a2a-multi-agent`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/a2a-multi-agent)（16 个 skill） |

---

## MPP（Machine Payments Protocol）

| 属性 | 说明 |
|------|------|
| **主导方** | Stripe、Tempo Labs |
| **官网** | [paymentauth.org](https://paymentauth.org)（IETF 草案） |
| **解决的问题** | 服务器/API 之间的自动付款（机器对机器），基于 HTTP 402，无需人工介入，适用于 AI Agent 自动为工具调用付费 |
| **核心机制** | HTTP 402 质询-响应流程；Charge Intent / Session Intent；Tempo 区块链 USDC 结算；Stripe SPT 集成；mppx SDK 封装 |
| **面向用户** | 🤖 AI（消费者侧）<br>🔧 开发者（后端） |
| **对应 Skill** | [OrcaQubits `stripe-mpp`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/stripe-mpp)（12 个 skill） |

---

## WebMCP（Web Model Context Protocol）

| 属性 | 说明 |
|------|------|
| **主导方** | Google、Microsoft、W3C |
| **官网** | [webmachinelearning.github.io/webmcp](https://webmachinelearning.github.io/webmcp/)（W3C 草案） |
| **解决的问题** | 让现有网站无需后端改造就能被 AI Agent 感知和操作，通过浏览器原生 API 暴露结构化工具 |
| **核心机制** | `navigator.modelContext` 浏览器 API；`registerTool`（声明可被 Agent 调用的操作）；声明式表单 HTML 属性注解；Human-in-the-Loop 确认流程 |
| **面向用户** | 🤖 AI（消费者侧）<br>🎨 开发者（前端） |
| **对应 Skill** | [OrcaQubits `webmcp-browser-agents`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/webmcp-browser-agents)（14 个 skill） |

---

## 协议 Skill 来源索引

| Repo | 协议 Skill 数量 | 许可证 |
|------|---------------|--------|
| [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins) | 100+ skill（5 个平台 + 6 个协议） | MIT |

---

*最后更新：2026 年 4 月 | 数据来源：各协议官网及 GitHub 文档*
