# 电商领域 CLI 工具全览

> 整理了 18 个与电商开发、运营、部署相关的命令行工具，涵盖电商平台、支付、搜索、基础设施等多个维度。

---

## 目录

- [电商平台 CLI](#-电商平台-cli)
- [支付 CLI](#-支付-cli)
- [数据 & 搜索 CLI](#-数据--搜索-cli)
- [基础设施 CLI](#-基础设施-cli)
- [云部署 CLI](#-云部署-cli)
- [开源框架 CLI](#-开源框架-cli)
- [面向用户说明](#面向用户说明)
- [快速选型建议](#快速选型建议)

---

## 🛍️ 电商平台 CLI

| CLI 工具 | 公司 | 官网 | 面向用户 | 核心能力 |
|---|---|---|---|---|
| **Shopify CLI** | Shopify | [shopify.dev/docs/api/shopify-cli](https://shopify.dev/docs/api/shopify-cli) | 开发者 | 应用脚手架生成、主题本地开发与热重载、Hydrogen 无头店铺创建、一键部署到 Shopify 平台、App OAuth 认证、本地扩展开发 |
| **Stencil CLI** | BigCommerce | [developer.bigcommerce.com](https://developer.bigcommerce.com/docs/storefront/stencil/cli) | 开发者 | 主题本地预览（Browsersync 多设备同步）、主题打包与推送、从线上 store 拉取配置、多 storefront/channel 一键部署 |
| **WC-CLI** (`wp wc`) | Automattic / WooCommerce | [developer.woocommerce.com/docs/wc-cli](https://developer.woocommerce.com/docs/wc-cli) | 商家、开发者 | CRUD 产品/变体/分类、管理订单与退款、客户管理、优惠券、税率配置、支付网关、配送区域、Webhook、数据库升级 |
| **WP-CLI** | WordPress.org | [wp-cli.org](https://wp-cli.org) | 商家、开发者 | 插件/主题安装更新、多站点管理、数据库导入导出、配置文件管理，是 WooCommerce CLI 的底层运行环境 |
| **bin/magento** | Adobe (Magento) | [experienceleague.adobe.com](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/config-cli) | 开发者 | 145 条命令：缓存管理、索引重建、模块启用/禁用、静态资源部署、数据库迁移、维护模式切换、Cron 调度、DI 编译 |
| **PrestaShop Console** | PrestaShop SA | [devdocs.prestashop-project.org](https://devdocs.prestashop-project.org) | 开发者 | 模块安装/卸载、缓存清理、数据库 schema 更新、基于 Symfony Console 的命令扩展 |
| **Shopware CLI** | Shopware AG | [developer.shopware.com](https://developer.shopware.com) | 开发者 | 插件管理、主题编译、系统版本升级、数据库迁移、缓存清理、店铺配置管理（支持 Shopware 5/6） |

---

## 💳 支付 CLI

| CLI 工具 | 公司 | 官网 | 面向用户 | 核心能力 |
|---|---|---|---|---|
| **Stripe CLI** | Stripe | [docs.stripe.com/stripe-cli](https://docs.stripe.com/stripe-cli) | 开发者 | 本地 Webhook 监听与转发、触发支付事件（成功/失败/退款/争议）、直接调用 Stripe REST API、生成测试数据、账户登录授权管理 |
| **Stripe Apps CLI** | Stripe | [docs.stripe.com/stripe-apps/reference/cli](https://docs.stripe.com/stripe-apps/reference/cli) | 开发者 | 创建/预览/上传 Stripe Dashboard 扩展应用、管理 App 权限与发布流程 |

---

## 🔍 数据 & 搜索 CLI

| CLI 工具 | 公司 | 官网 | 面向用户 | 核心能力 |
|---|---|---|---|---|
| **Algolia CLI** | Algolia | [algolia.com/doc/tools/cli](https://algolia.com/doc/tools/cli/get-started) | 商家、开发者 | 管理搜索索引、批量导入/导出商品数据、调整搜索排名规则与同义词、管理 API Key 权限 |
| **Contentful CLI** | Contentful | [contentful.com/developers/docs/tutorials/cli](https://www.contentful.com/developers/docs/tutorials/cli/) | 开发者 | 导入/导出 content model 与数据、多环境迁移脚本、Space 管理、商品多语言内容自动化发布 |

---

## ☁️ 基础设施 CLI

| CLI 工具 | 公司 | 官网 | 面向用户 | 核心能力 |
|---|---|---|---|---|
| **Vercel CLI** | Vercel | [vercel.com/docs/cli](https://vercel.com/docs/cli) | 开发者 | 独立站前端部署与预览环境、环境变量管理、域名绑定、Serverless Functions 本地调试、团队项目协作 |
| **Netlify CLI** | Netlify | [docs.netlify.com/cli](https://docs.netlify.com/cli/get-started/) | 开发者 | 本地开发服务器（含 Edge Functions）、站点部署与回滚、环境变量/插件管理、无头电商前端构建与测试 |
| **Firebase CLI** | Google | [firebase.google.com/docs/cli](https://firebase.google.com/docs/cli) | 开发者 | 小程序/App 电商后端部署、Firestore 规则管理、Cloud Functions 本地测试、Hosting 静态部署 |

---

## 🖥️ 云部署 CLI

| CLI 工具 | 公司 | 官网 | 面向用户 | 核心能力 |
|---|---|---|---|---|
| **Magento Cloud CLI** | Adobe | [experienceleague.adobe.com](https://experienceleague.adobe.com/en/docs/commerce-on-cloud) | 开发者 | 123 条命令：环境分支与部署、SSH 访问、MySQL/Redis 服务隧道、快照备份恢复、CI/CD 非交互模式、多环境管理 |
| **AWS CLI** | Amazon | [aws.amazon.com/cli](https://aws.amazon.com/cli/) | 开发者 | S3 产品图片存储管理、Lambda 函数部署、CloudFront CDN 配置、DynamoDB 订单数据操作、ECS 容器编排 |

---

## 🧱 开源框架 CLI

| CLI 工具 | 公司 | 官网 | 面向用户 | 核心能力 |
|---|---|---|---|---|
| **Medusa CLI** | Medusa (medusajs.com) | [docs.medusajs.com/resources/medusa-cli](https://docs.medusajs.com/resources/medusa-cli) | 开发者 | `create-medusa-app` 项目脚手架、`develop/start/build` 应用生命周期管理、`exec` 执行自定义脚本、plugin 插件发布/安装、db 迁移生成 |
| **Saleor CLI (Configurator)** | Saleor Commerce | [saleor.io](https://saleor.io) | 开发者 | Configurator CLI：与 GraphQL API 同步 store 配置、CI/CD 自动化部署、版本化配置管理、商品模型导入导出 |

---

## 面向用户说明

| 标签 | 说明 |
|---|---|
| 🟢 **商家** | 运营人员可直接上手，用于管理产品、订单、配置等日常运营任务 |
| 🔵 **开发者** | 主要面向开发者，用于本地开发、部署自动化、系统集成等技术场景 |

> **注意**：大多数电商 CLI 工具面向开发者设计。商家通常通过 Admin 界面操作，只有少数 CLI（如 WP-CLI、WC-CLI、Algolia CLI）在运营工作中被直接使用。

---

## 快速选型建议

| 使用场景 | 推荐工具 |
|---|---|
| Shopify 生态应用/主题开发 | **Shopify CLI** |
| BigCommerce 主题开发 | **Stencil CLI** |
| WooCommerce 店铺自动化与运维 | **WP-CLI** + **WC-CLI** |
| Magento/Adobe Commerce 大型站运维 | **bin/magento** + **Magento Cloud CLI** |
| 支付集成本地开发与测试 | **Stripe CLI** |
| 商品搜索索引管理 | **Algolia CLI** |
| 无头电商前端部署（Vercel） | **Vercel CLI** |
| 开源无头电商后端开发（Node.js） | **Medusa CLI** |
| 开源无头电商后端开发（Python） | **Saleor CLI** |
| AWS 云资源管理（S3、CDN、Lambda） | **AWS CLI** |

---

## 安装示例

```bash
# Shopify CLI
npm install -g @shopify/cli

# BigCommerce Stencil CLI
npm install -g @bigcommerce/stencil-cli

# WP-CLI
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
chmod +x wp-cli.phar && mv wp-cli.phar /usr/local/bin/wp

# Stripe CLI (macOS)
brew install stripe/stripe-cli/stripe

# Medusa CLI
npm install -g @medusajs/medusa-cli

# Vercel CLI
npm install -g vercel

# AWS CLI
pip install awscli
```

---

*最后更新：2026 年 4 月 | 数据来源：各平台官方文档*
