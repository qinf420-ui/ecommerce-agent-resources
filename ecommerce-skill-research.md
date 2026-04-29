# 电商领域 Skill / MCP / 协议 调研报告

> **调研时间**：2026 年 4 月  
> **数据来源**：逐一 fetch 各 GitHub repo 的 README 及 SKILL.md 原文  
> **最小单元**：每个独立的 SKILL.md 文件

---

## 目录

- [A. Skill](#a-skill)
  - [A1. 店铺前台开发](#a1-店铺前台开发)
  - [A2. 店铺后台开发](#a2-店铺后台开发)
  - [A3. 商品 & 目录管理](#a3-商品--目录管理)
  - [A4. 订单 & 履行](#a4-订单--履行)
  - [A5. 客户管理](#a5-客户管理)
  - [A6. 支付 & 结账](#a6-支付--结账)
  - [A7. 数据分析 & 财务诊断](#a7-数据分析--财务诊断)
  - [A8. 营销 & CRO](#a8-营销--cro)
  - [A9. 部署 & 运维](#a9-部署--运维)
- [B. MCP Server](#b-mcp-server)
  - [B1. 店铺数据读写](#b1-店铺数据读写)
  - [B2. 支付操作](#b2-支付操作)
  - [B3. 数据采集](#b3-数据采集)
  - [B4. 客服自动化](#b4-客服自动化)
- [C. Agentic Commerce 协议](#c-agentic-commerce-协议)
- [附录：来源索引](#附录来源索引)

---

## A. Skill

### A1. 店铺前台开发

面向主题、模板、UI 组件、前端展示层的开发 skill。

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-liquid` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-liquid)（官方） | Liquid 模板与主题开发，包含语法规范、Online Store 2.0 主题结构及代码验证 | Liquid 语法（变量/过滤器/控制流）；Online Store 2.0 主题结构（sections/blocks/snippets）；Dawn/Horizon 主题扩展；Schema JSON 与主题设置面板；Liquid schema 代码验证 | Shopify | 开发者 |
| `shopify-hydrogen` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-hydrogen)（官方） | Shopify 官方 React 无头框架开发，适用于高度定制化的无头店铺构建 | Hydrogen + Remix 项目脚手架；Storefront API 数据获取（产品/集合/购物车）；Server/Client Component 架构；Oxygen 云端部署；图片懒加载与 Streaming SSR 性能优化 | Shopify | 开发者 |
| `shopify-polaris-checkout-extensions` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-polaris-checkout-extensions)（官方） | 在 Shopify 结账页面嵌入自定义 UI 组件，支持礼品留言、追加销售等扩展场景 | Checkout Extension 目标点注册；Polaris UI 组件在结账中的规范用法；useApplyAttributeChange/useCartLines Hooks；App Bridge 双向通信；礼品留言/自定义字段/追加销售组件 | Shopify | 开发者 |
| `shopify-polaris-customer-account-extensions` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-polaris-customer-account-extensions)（官方） | 在客户账户页面嵌入自定义 UI，展示订单历史、积分状态等会员专属信息 | 客户账户页面 UI 自定义；Customer Account API 数据访问；忠诚度积分/会员状态展示组件；Extension 目标点注册与渲染 | Shopify | 开发者 |
| `shopify-polaris-app-home` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-polaris-app-home)（官方） | App Home 页面 UI 规范，用于开发者构建符合 Shopify 设计语言的 App 首页 | App Home 设计规范；Polaris 组件使用模式；Onboarding 引导流程/Action Card/Banner；与 Admin API 的数据联动 | Shopify | 开发者 |
| `shopify-pos-ui` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-pos-ui)（官方） | Shopify POS 线下收银 App 的 UI 扩展开发，支持 Cart 扩展和自定义收银操作 | POS UI Extension（Cart 扩展/Action 扩展）；POS 硬件交互（打印机/扫码枪）；线下收银自定义插件；线下库存与线上库存同步展示 | Shopify POS | 开发者 |
| `bigcommerce-stencil` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/bigcommerce-commerce) | BigCommerce 主题框架本地开发，支持多 storefront 定制与一键部署 | Stencil CLI 本地开发环境；Handlebars 模板语法与主题变量；Cornerstone 主题扩展；多 storefront/channel 主题推送；Browsersync 多设备实时预览 | BigCommerce | 开发者 |
| `magento-frontend` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 前端主题开发，覆盖 Luma 主题继承、样式编译与 KnockoutJS 数据绑定 | Luma/Blank 主题继承与覆写；Less 样式编译与自定义变量；RequireJS 模块配置；KnockoutJS 数据绑定（Mini Cart/产品页）；UI Component XML 配置 | Magento 2 | 开发者 |
| `woocommerce-frontend` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 前端集成开发，支持主题模板覆写、Gutenberg Block 与 React 组件扩展 | WooCommerce 模板覆写机制（woocommerce/ 目录）；子主题样式集成；Gutenberg Block 开发（产品卡片/Cart Block）；React 组件集成前端 | WooCommerce | 开发者 |
| `salesforce-pwa-kit` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/salesforce-commerce) | Salesforce B2C Commerce 无头店铺开发，使用 React + Commerce SDK 构建 PWA | PWA Kit 项目初始化与路由；Commerce SDK 数据获取；Service Worker 离线支持；ManagedRuntime 云端部署 | Salesforce Commerce Cloud | 开发者 |
| `discover-rule-topics` | [TeamDijon/shopify-rules](https://github.com/TeamDijon/shopify-rules/blob/main/.claude/skills/discover-rule-topics/SKILL.md) | 挖掘 Shopify 主题代码模式，构建 AI 可用的主题开发规则知识库 | 跨主题挖掘 CSS/JavaScript/Liquid 共性模式；Dawn/Horizon 主题对比分析；主题规则知识库构建 | Shopify（主题开发） | 开发者 |

---

### A2. 店铺后台开发

面向 App 开发、插件/模块、Admin UI 定制和平台后端逻辑的 skill。

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-admin` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-admin)（官方） | Shopify Admin GraphQL API 的完整查询与变更能力，内置 schema 验证和文档搜索 | Admin GraphQL API 查询/mutation（产品/订单/客户/库存）；代码级 schema 实时验证；离线 GraphQL schema 内嵌参考；shopify.dev 文档搜索；Bulk Operations 异步大数据集操作 | Shopify | 开发者 |
| `shopify-app-development` | [christophacham/agent-skills-library](https://github.com/christophacham/agent-skills-library/blob/main/skills/web-dev/shopify-development/SKILL.md) | Shopify 全栈 App 开发，覆盖 OAuth 认证、GraphQL 操作、Webhook 和 Billing API 变现 | App 类型决策树（App/Extension/Theme）；OAuth 认证流程；GraphQL mutation（产品/订单/账单）；Webhook HMAC 验证；Billing API 订阅收费集成 | Shopify | 开发者 |
| `shopify-polaris-admin-extensions` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-polaris-admin-extensions)（官方） | 在 Shopify Admin 后台添加自定义 UI 块和操作按钮，扩展商品详情页、订单页等管理界面 | Admin Action Extension（后台操作按钮）；Admin Block Extension（自定义信息面板）；Polaris 组件规范；App Bridge 与 Admin 双向通信；Extension 部署与预览 | Shopify | 开发者 |
| `shopify-functions` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-functions)（官方） | 通过 Wasm 编写的 Shopify Functions，在购物车、折扣、配送、支付等环节注入自定义逻辑 | Cart Transform Function；Discount Function（自定义折扣规则）；Delivery Customization（过滤配送选项）；Payment Customization（隐藏/排序支付方式）；GraphQL input query 选取 Function 输入数据 | Shopify | 开发者 |
| `shopify-custom-data` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-custom-data)（官方） | 使用 Metafield 和 Metaobject 为 Shopify 数据模型添加自定义字段，支持产品、客户、订单等对象扩展 | shopify.app.toml 定义 Metafield/Metaobject schema；metafieldsSet/metaobjectUpsert 写入；Admin API/Storefront API 读取（jsonValue）；Checkout Extension 直接访问 app-owned metafields；Functions input query 选取 metafield | Shopify | 开发者 |
| `shopify-api`（社区） | [Microck/ordinary-claude-skills](https://github.com/Microck/ordinary-claude-skills/blob/main/skills_all/shopify-api/SKILL.md) | Shopify 全 API 集成参考，覆盖 Admin、Storefront、Ajax、OAuth 和 Webhook，基于 2025-10 版本 | GraphQL Admin API（2025-10）；REST Admin API；Storefront API（产品/购物车/结账）；Ajax API 前端购物车操作；OAuth 完整授权流程；速率限制处理（指数退避）；Webhook 签名验证 | Shopify | 开发者 |
| `shopify-partner` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-partner)（官方） | 通过 Partner API 管理合作伙伴组织下的 App 数据、安装量、收益及开发商店 | Partner API 查询 App 安装量/收益；合作伙伴组织多 App 管理；Development Store 创建与管理；App 审核状态查询 | Shopify Partner | 开发者 |
| `shopify-app-store-review` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-app-store-review)（官方） | Shopify App Store 上架前的合规检查与 listing 优化 | App Store 上架规范检查；listing 文案与截图规范；审核常见拒绝原因与解决方案；Privacy Policy/ToS 合规性检查 | Shopify | 开发者 |
| `magento-module-dev` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 模块开发，从目录结构到路由、控制器、Block 的完整创建流程 | 模块目录结构规范；registration.php/module.xml/composer.json 生成；路由/控制器/Block 创建；ViewModel 与 Layout XML 配置 | Magento 2 | 开发者 |
| `magento-di` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 依赖注入配置，通过 di.xml 管理类型、参数和首选项 | di.xml 配置（type/argument/preference/virtualType）；Constructor 注入 vs. 方法注入；Proxy/Factory 类使用；setup:di:compile 依赖关系分析 | Magento 2 | 开发者 |
| `magento-plugins-interceptors` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 插件拦截器模式，在不覆盖核心代码的前提下修改任意方法行为 | before/after/around 方法命名规范；di.xml 注册 plugin；Plugin 链式调用与 proceed()；适用场景（价格修改/权限检查/日志注入） | Magento 2 | 开发者 |
| `magento-service-contracts` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 服务契约模式，通过 Repository Interface 和 Data Interface 实现稳定的 API 层 | Repository Interface 设计（CRUD 标准方法）；Data Interface 与 Extension Attributes；SearchCriteria/FilterGroup 查询；webapi.xml 暴露 REST/SOAP 接口 | Magento 2 | 开发者 |
| `magento-eav-attributes` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 EAV 属性系统，为产品、客户、分类添加自定义数据字段 | EAV 属性创建（安装脚本/UpgradeData）；属性类型（text/select/multiselect/boolean/price）；产品/客户/分类属性添加到 Admin 表单；Attribute Set 与 Attribute Group 管理 | Magento 2 | 开发者 |
| `magento-admin-ui` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 Admin 后台 UI 开发，包含列表页 Grid、编辑页 Form 及权限控制 | UI Component Grid XML 配置；UI Component Form 字段与验证；ACL 权限资源注册（acl.xml）；Admin 菜单配置（menu.xml） | Magento 2 | 开发者 |
| `woocommerce-plugin-dev` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 插件开发基础，覆盖插件结构、激活/停用 Hook 及与 WooCommerce 的集成声明 | 插件目录结构与主文件头规范；register_activation_hook/register_deactivation_hook；WooCommerce 集成声明（woocommerce_init）；依赖检查与版本兼容性处理 | WooCommerce | 开发者 |
| `woocommerce-hooks-filters` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 钩子与过滤器系统，无需修改核心代码即可自定义任意商业逻辑 | Action hooks（before_cart/payment_complete 等）；Filter hooks（product_price/add_to_cart_validation 等）；Hook 优先级与参数数量配置；常用商业逻辑 hooks 速查表 | WooCommerce | 开发者 |
| `woocommerce-admin` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 后台管理页面定制，添加设置页、自定义列及 Meta Box | WooCommerce 设置 Tab/Section 添加；产品列表页自定义列与批量操作；订单详情页 Meta Box；WooCommerce Admin React 组件扩展 | WooCommerce | 开发者 |
| `bigcommerce-app-dev` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/bigcommerce-commerce) | BigCommerce 单次点击 App 开发，覆盖 OAuth 安装、iFrame 渲染和 Webhook 订阅 | Single-Click App OAuth 安装流程；App Bridge iFrame 渲染；Webhook 订阅（订单/产品/客户事件）；Partner Portal 上架流程 | BigCommerce | 开发者 |
| `salesforce-sfra` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/salesforce-commerce) | Salesforce B2C Commerce SFRA 开发，通过 Cartridge 覆写机制扩展电商功能 | Cartridge 覆写机制与 Cartridge Path 配置；Controller 路由与 Route 扩展；ISML 模板语法；Page Designer 内容组件开发 | Salesforce Commerce Cloud | 开发者 |
| `medusa-setup` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/medusa-commerce) | Medusa 开源无头电商后端项目初始化与开发环境配置 | create-medusa-app 脚手架；数据库连接配置（PostgreSQL/Supabase）；本地开发服务器启动（medusa develop）；Plugin 安装与本地测试 | Medusa | 开发者 |

---

### A3. 商品 & 目录管理

面向产品 CRUD、库存、价格、SEO、分类的操作型 skill。

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-products` | [jezweb/claude-skills](https://github.com/jezweb/claude-skills/blob/main/plugins/shopify/skills/shopify-products/SKILL.md) | 通过 Shopify Admin API 创建和管理产品，支持单品操作与 CSV 批量导入 | GraphQL productCreate/productUpdate mutation；变体（Variants）选项/SKU/价格/库存管理；图片两步上传（staged upload → attach）；批量导入（CSV + Bulk Operations JSONL）；产品与 Collection 关联 | Shopify | 商家、开发者 |
| `shopify-content` | [jezweb/claude-skills](https://github.com/jezweb/claude-skills/blob/main/plugins/shopify/skills/shopify-content/SKILL.md) | 管理 Shopify 店铺内容，包括静态页面、博客文章、导航菜单和 SEO 元数据 | GraphQL pageCreate/pageUpdate（About/FAQ 等静态页面）；articleCreate（博客文章，支持定时发布）；SEO 元数据更新（title/description）；Navigation 菜单管理；URL Redirect 批量管理 | Shopify | 商家、开发者 |
| `shopify-admin`（社区，媒体） | [askphill/ww](https://github.com/askphill/ww/blob/main/.claude/skills/shopify-admin/SKILL.md) | 通过 shell 脚本封装的 Shopify Admin 数据查询与媒体文件上传 | 产品/文件/图片/视频查询（分页与搜索）；媒体文件上传（jpg/png/gif/mp4/pdf 等） | Shopify | 商家、开发者 |
| `shopify-onboarding-merchant` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-onboarding-merchant)（官方） | 面向 Shopify 商家的店铺初始化引导，覆盖首批产品上架和基础配置 | 新店铺初始化（支付/配送/税务）；首批产品上架引导（手动/批量导入）；域名配置与 SSL；主题选择与 Logo 设置 | Shopify | 商家 |
| `magento-catalog` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 商品目录管理，支持多种产品类型、分类树、价格规则和 MSI 库存 | 产品类型创建（Simple/Configurable/Bundle/Grouped/Virtual）；分类树管理（CategoryRepositoryInterface）；目录价格规则配置；MSI 多仓库存分配；价格索引重建 | Magento 2 | 开发者 |
| `woocommerce-catalog` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 商品目录管理，通过代码创建产品、变体、属性和分类 | WC_Product_Simple/Variable 程序化创建；产品属性（Attribute）与变体（Variation）管理；产品分类（Term）与标签；价格字段与 Scheduled Sale | WooCommerce | 开发者 |
| `bigcommerce-catalog` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/bigcommerce-commerce) | BigCommerce 商品目录 API 操作，支持 REST 和 GraphQL 双模式及 B2B 分级定价 | REST Catalog API 产品 CRUD；产品变体/modifier/选项管理；Price Lists（B2B 分级定价）；品牌（Brand）与分类树管理 | BigCommerce | 开发者 |

---

### A4. 订单 & 履行

面向订单处理、退款、发货、物流状态的操作型 skill。

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `fulfillment-ops`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/fulfillment-ops) | 包含 5 个履行操作 skill，覆盖日报、Hold、智能路由、追踪更新和 SLA 监控 | 履行状态日报生成（待处理/已发货/延迟）；订单 Hold/Release（orderHoldCreate/orderHoldRelease）；智能路由到最优库位；批量更新追踪号（fulfillmentTrackingInfoUpdateV2）；SLA 违约订单预警 | Shopify | 商家 |
| `customer-support`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/customer-support) | 包含 5 个客服操作 skill，覆盖订单查询、退款、退货申请、地址修改和 WISMO 自动回复 | 通过邮箱/订单号查询订单状态；全额/部分退款处理（refundCreate，dry_run 预览后执行）；退货申请发起（returnCreate）；发货前地址修改（orderUpdate）；WISMO 自动回复模板生成 | Shopify | 商家 |
| `returns`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/returns) | 包含 3 个退货分析 skill，覆盖退货原因分析、换货比率计算和 SLA 监控 | 退货原因分布分析（损坏/尺码/不符/改变主意）；换货 vs 退款比例报告；退款处理 SLA 违约标记 | Shopify | 商家 |
| `order-intelligence`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/order-intelligence) | 包含 3 个订单智能分析 skill，覆盖欺诈评分、高风险打标和复购识别 | Shopify Fraud Analysis API 欺诈评分；高风险订单自动打标（tagsAdd）；复购用户识别与购买间隔分析 | Shopify | 商家 |
| `magento-checkout` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 结账流程定制，包含步骤定制、地址字段扩展和订单事件监听 | Checkout 步骤添加/修改（checkout_index_index.xml）；地址表单字段自定义；订单属性扩展（Extension Attributes）；购物车价格规则；订单事件监听（checkout_submit_all_after） | Magento 2 | 开发者 |
| `woocommerce-checkout` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 结账流程定制，支持 Blocks API 和 Classic Checkout 双模式 | WooCommerce Blocks API 自定义结账字段；Classic Checkout hooks（woocommerce_checkout_fields/process）；结账字段保存到 Order Meta；订单状态流转 | WooCommerce | 开发者 |

---

### A5. 客户管理

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-customer` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-customer)（官方） | Shopify Customer Account API 开发，支持客户自助服务功能和 B2B 公司账户数据访问 | Customer Account API OAuth PKCE 认证；客户订单历史查询（customer.orders）；地址管理（customerAddress* mutations）；客户账户偏好设置；B2B 公司账户数据访问 | Shopify | 开发者 |
| `customer-ops`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/customer-ops) | 包含 6 个客户运营 skill，覆盖去重、分层打标、同期群分析、B2B 配置和 GDPR 处理 | 重复客户账户检测（按邮箱/电话）；按生命周期消费分层打标（Bronze/Silver/Gold/VIP）；客户同期群留存与 LTV 分析；B2B 公司账户与联系人配置；GDPR 删除请求处理（customerRequestDataErasure）；VIP 客户自动识别与打标 | Shopify | 商家 |
| `woocommerce-data-stores`（含客户） | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce CRUD 数据层操作，通过官方 API 管理客户、订单、产品数据，兼容 HPOS | WC_Customer CRUD（注册/地址/元数据）；HPOS 高性能订单存储兼容；Customer Meta 自定义字段读写 | WooCommerce | 开发者 |

---

### A6. 支付 & 结账

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-payments-apps` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-payments-apps)（官方） | 开发 Shopify 自定义支付方式 App，实现完整的支付创建、捕获、作废和退款流程 | Payments App Extension 开发；Payment Session 创建与解析；Capture/Void/Refund 操作实现；支付 App 合规性要求与测试；shopify.app.toml Payments 配置 | Shopify | 开发者 |
| `payment-integration` | [mrgoonie/claudekit-skills](https://github.com/mrgoonie/claudekit-skills) | 多支付平台综合集成方案，覆盖 Stripe、Paddle、Polar 及越南本地支付 SePay | Stripe Checkout Session/Customer Portal/Webhook 验证；Paddle 订阅与 Merchant of Record；Polar 开源项目变现；SePay 越南 VietQR 集成；通用 Webhook 签名验证模式 | 通用（Shopify/SaaS） | 开发者 |
| `woocommerce-payments` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/woocommerce-commerce) | WooCommerce 支付网关开发，实现自定义支付方式和信用卡 Token 化存储 | WC_Payment_Gateway 子类实现（process_payment/validate_fields）；信用卡 Token 化（WC_Payment_Token）；Webhook 处理（成功/失败/退款）；Stripe Elements/PayPal SDK 集成模式 | WooCommerce | 开发者 |
| `bigcommerce-payments` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/bigcommerce-commerce) | BigCommerce 支付集成，通过 Checkout SDK 定制结账流程和支付方式配置 | BigCommerce Checkout SDK 自定义；支付方式隐藏/排序（Payments API）；第三方支付服务商对接（Klarna/Afterpay 等 BNPL） | BigCommerce | 开发者 |

---

### A7. 数据分析 & 财务诊断

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `claude-ecom` | [takechanman1228/claude-ecom](https://github.com/VoltAgent/awesome-agent-skills)（经 awesome-agent-skills 收录） | 从订单 CSV 自动生成完整电商业务回顾，输出 KPI 分解树、诊断摘要和行动计划 | 从订单 CSV 提取核心 KPI（GMV/AOV/转化率/复购率）；KPI 分解树（收入 = 流量 × 转化 × AOV）；按优先级排列的诊断发现摘要；针对数据异常点的具体行动计划 | 通用（任意能导出 CSV 的平台） | 电商运营、商家 |
| `ecom-cfo-skill` | [jeffreydebolt/ecom-cfo-skill](https://github.com/jeffreydebolt/ecom-cfo-skill) | 适用于 $50万–$3000万规模电商的兼职 CFO 诊断框架，覆盖 Amazon、Shopify 和混合渠道卖家 | 瀑布诊断法（COGS→履行→毛利→广告→净利润逐层排查）；贡献利润阈值体系（15%/20%/25%）；TRIAGE.md 快速诊断卡；THRESHOLDS.md 行业基准参考；COMMON_FAILURES.md 常见问题模式；多客户只读财务 Copilot 架构 | Amazon、Shopify、混合渠道 | 电商创始人、CFO、财务顾问 |
| `finance`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/finance) | 包含 7 个财务报表 skill，覆盖收入、退款率、AOV、税务、配送成本等维度 | 按渠道/产品/日期的收入拆分报告；退款率趋势与驱动因素分析；AOV 趋势追踪；多税区税务负债汇总；配送成本率分析；折扣码收入影响评估 | Shopify | 商家 |
| `conversion-optimization`（系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/conversion-optimization) | 包含 3 个转化优化分析 skill，覆盖折扣 A/B 测试、弃购分析和礼品卡追踪 | 折扣金额/比例 A/B 测试报告；购物车与结账弃购率漏斗分析；礼品卡使用与剩余负债追踪 | Shopify | 商家 |

---

### A8. 营销 & CRO

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `marketing`（弃购/会员系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/marketing) | 包含 3 个营销运营 skill，覆盖弃购购物车标记、流失客户挽回和忠诚度会员导出 | 弃购购物车识别与客户打标（checkouts GraphQL 查询）；流失客户名单导出（按消费分层）；积分/忠诚度计划资格客户导出 | Shopify | 商家 |
| `merchandising`（商品化系列） | [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills/tree/main/skills/merchandising) | 包含 18 个商品运营 skill，覆盖批量定价、库存盘点、SEO 优化、滞销分析等 | 按规则批量调价；库存盘点与异常标记；产品 SEO title 批量优化；死库存/滞销库存识别；Collection 产品排序规则；Metafield 批量写入；条件批量打标 | Shopify | 商家 |
| `page-cro` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 落地页与注册/激活流程的转化率优化诊断 | 落地页 CTA/社会证明/价值主张诊断；注册/激活流程摩擦点识别；A/B 测试假设生成；转化漏斗分析框架 | 通用（含电商落地页） | 电商运营、增长团队 |
| `email-sequence` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 电商邮件序列设计，覆盖欢迎、弃购挽回和复购激活场景 | 欢迎邮件序列（5-7 封）结构设计；弃购挽回邮件时间节点与内容框架；复购激活序列（休眠客户）；邮件主题行 A/B 测试建议 | 通用（与任意 ESP 配合） | 电商运营 |
| `seo-audit` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 电商网站 SEO 诊断，包含技术 SEO、产品页优化和结构化数据实施 | 技术 SEO 诊断（Page Speed/Core Web Vitals/结构化数据）；产品页/分类页关键词优化；站内链接结构审查；Product/BreadcrumbList Schema Markup 实施 | 通用（含 Shopify/WooCommerce） | 电商运营 |
| `analytics-tracking` | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | GA4 电商事件埋点配置，覆盖完整购物漏斗追踪与 GTM 设置 | GA4 电商事件（view_item/add_to_cart/purchase）；GTM Container 触发器配置；转化漏斗事件验证；购物行为报告设置 | 通用（含 Shopify/WooCommerce） | 电商运营、开发者 |

---

### A9. 部署 & 运维

| Skill 名称 | Repo | Skill 描述（中文） | 支持的能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-setup` | [jezweb/claude-skills](https://github.com/jezweb/claude-skills/blob/main/plugins/shopify/skills/shopify-setup/SKILL.md) | Shopify CLI 认证与 Admin API Access Token 获取，为产品和内容管理建立稳定 API 连接 | Shopify CLI 安装与 OAuth 登录；自定义 App 创建流程（含浏览器自动化辅助）；Admin API Access Token 安全存储（.dev.vars）；API Scope 选择指南；API 版本季度轮换策略 | Shopify | 开发者 |
| `shopify-onboarding-dev` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-onboarding-dev)（官方） | 面向 Shopify 开发者的环境初始化，从 Partner 账号到 App 创建、开发商店配置的完整链路 | Partner Dashboard 账户与 App 创建；Development Store 配置；Shopify CLI 开发环境初始化（shopify app init/dev）；本地开发隧道配置 | Shopify | 开发者 |
| `shopify-dev` | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit/tree/main/skills/shopify-dev)（官方） | Shopify 开发者文档全站搜索，用于解答 API 版本、废弃字段等非特定场景的通用开发问题 | shopify.dev 文档全站搜索（scripts/search_docs.js）；API 版本与废弃字段查询；通用开发问题诊断 | Shopify | 开发者 |
| `magento-performance` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 性能调优，覆盖缓存策略、索引优化、数据库和 Redis/Varnish 配置 | FPC + Varnish VCL 配置；Redis 会话/缓存配置；索引器模式优化（realtime → schedule）；数据库慢查询分析；Flat Catalog 与 Layered Navigation 索引优化 | Magento 2 | 开发者 |
| `magento-deploy` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 生产部署流程，包含静态文件部署、DI 编译和零停机部署方案 | 生产模式切换与静态文件部署（setup:static-content:deploy）；DI 编译（setup:di:compile）与维护模式管理；零停机蓝绿部署方案；Magento Cloud CLI 环境管理 | Magento 2 | 开发者 |
| `magento-security` | [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/magento2-commerce) | Magento 2 安全加固，覆盖 PCI-DSS 合规、Admin 保护、CSP 配置和常见漏洞防护 | Admin URL 自定义与双因素认证（2FA）；CSP 配置；PCI-DSS 合规检查清单；SQL 注入与 XSS 防护；安全补丁应用流程 | Magento 2 | 开发者 |

---

## B. MCP Server

MCP Server 是实时 API 连接层，让 AI Agent 通过自然语言直接执行店铺操作，与 Skill（指令包）不同，MCP 需要 API 凭证才能访问真实数据。

### B1. 店铺数据读写

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `shopify-mcp` | [GeLi2001/shopify-mcp](https://github.com/GeLi2001/shopify-mcp)  npm: `shopify-mcp` | 最活跃的 Shopify MCP，基于 GraphQL Admin API 2026-01，支持 OAuth 和 Access Token 双认证 | 产品管理 8 个工具（CRUD 产品/变体/选项）；客户管理 8 个工具（CRUD/合并/地址）；订单管理 10 个工具（查询/取消/关闭/标记已付款/履行/退款）；Metafield 管理 3 个工具；库存管理 1 个工具；标签管理 1 个工具 | Shopify | 商家、开发者 |
| `Shopify Dev MCP`（官方） | [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit)  npm: `@shopify/dev-mcp` | Shopify 官方开发文档 MCP，实时搜索 shopify.dev 文档，不直接操作店铺数据 | shopify.dev 全站文档搜索；API 字段/schema/示例代码查询；API 版本与废弃字段确认 | Shopify | 开发者 |
| `shopify-admin`（社区，媒体操作） | [askphill/ww](https://github.com/askphill/ww/blob/main/.claude/skills/shopify-admin/SKILL.md) | shell 脚本封装的轻量级 Shopify Admin 操作，专注媒体资产管理 | 产品查询（搜索/分页）；文件/图片/视频查询；媒体文件上传（jpg/png/gif/webp/svg/mp4/mov/pdf） | Shopify | 商家、开发者 |

---

### B2. 支付操作

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `Stripe MCP`（官方） | [Stripe 官方 MCP Registry](https://github.com/mcp)  可在 Claude.ai 直接连接 | Stripe 官方 MCP，覆盖客户、产品、支付、退款和订阅的完整管理 | 客户查询与创建；产品/价格管理；PaymentIntent 状态查询；退款处理；订阅管理；Webhook 端点管理 | 通用 | 开发者 |

---

### B3. 数据采集

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `Apify MCP` | [apify/apify-mcp-server](https://github.com/apify/apify-mcp-server)  URL: `https://mcp.apify.com`（支持 OAuth，Claude.ai 可直连） | 8000+ Actors 的数据采集 MCP，覆盖主流电商平台的产品、评论、价格数据抓取 | 亚马逊产品/评论/搜索数据爬取；竞品价格监控；社交电商数据（TikTok Shop/Instagram）；Google Shopping 数据抓取；8000+ 专项 Actor 按需调用 | 通用（多平台） | 商家、开发者 |

---

### B4. 客服自动化

| MCP 名称 | Repo / 来源 | 描述 | 支持的工具能力 | 适用平台 | 适用人群 |
|---|---|---|---|---|---|
| `Enneagora MCP` | [slavpilus/mcp](https://github.com/slavpilus/mcp) | 平台无关的电商客服 MCP，14 个工具覆盖从订单查询到售后政策的完整客服场景 | 订单查询/追踪/状态更新（4 个工具）；退货政策/配送信息/联系方式问答（4 个工具）；尺码指南/保修/产品护理信息（3 个工具）；支付方式/账户帮助/积分计划（3 个工具） | 通用（Shopify/Magento 策略层规划中） | 商家 |

---

## C. Agentic Commerce 协议

协议是**技术标准规范**，不是 Skill 也不是 MCP。它们定义 AI Agent 如何安全地代替人类完成商务交易的通信方式与授权机制。

| 协议 | 主导方 | 官网 | 解决的问题 | 核心机制 | 与 Skill 的对应实现 |
|---|---|---|---|---|---|
| **UCP**（Universal Commerce Protocol） | Google、Shopify，联合 Etsy/Wayfair/Target/Walmart | [ucp.dev](https://ucp.dev) | 构建从商品发现到结账到订单追踪的完整 Agent 购物旅程标准接口，消除 N×M 定制集成问题 | Product Search（产品搜索）；Unified Checkout（统一结账，支持动态定价和税务）；Identity Linking（OAuth 2.0 连接 Agent 与用户账户）；Order Management Webhook | [OrcaQubits `ucp-agentic-commerce`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/ucp-agentic-commerce)（15 个 skill） |
| **ACP**（Agentic Commerce Protocol） | OpenAI、Stripe | [agenticcommerce.dev](https://agenticcommerce.dev) | 让 AI Agent 在对话界面直接完成购买，确保 Agent 不接触用户支付凭证（PCI 合规） | Shared Payment Token（SPT）：一次性支付令牌，Agent 传递令牌不持有卡号；Agentic Checkout API：商家实现 create/update/complete/cancel 四个端点；Delegated Payment：Stripe 作为支付中间人 | [OrcaQubits `acp-agentic-commerce`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/acp-agentic-commerce)（15 个 skill） |
| **AP2**（Agent Payments Protocol） | Google | [ap2-protocol.org](https://ap2-protocol.org) | 当 AI Agent 自主购物时，提供可加密验证的"用户已授权"证明，解决无人值守场景的支付纠纷 | Intent Mandate（预授权，如"价格低于 ¥500 时自动购票"）；Cart Mandate（特定购物车明确授权，用户签名不可抵赖）；Payment Mandate（支付网络风险评估信号）；所有 Mandate 均使用加密签名 | [OrcaQubits `ap2-agentic-payments`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/ap2-agentic-payments)（18 个 skill） |
| **A2A**（Agent-to-Agent Protocol） | Google（现 Linux Foundation 维护） | [a2a-protocol.org](https://a2a-protocol.org) | 不同公司、不同框架构建的 AI Agent 之间如何互相发现能力、委托任务和传递上下文 | Agent Card（能力声明）；Task Lifecycle（任务状态机）；JSON-RPC Transport（标准通信格式）；Push Notifications（异步任务通知） | [OrcaQubits `a2a-multi-agent`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/a2a-multi-agent)（16 个 skill） |
| **MPP**（Machine Payments Protocol） | Stripe、Tempo Labs | [paymentauth.org](https://paymentauth.org)（IETF 草案） | 服务器/API 之间的自动付款（机器对机器），基于 HTTP 402，无需人工介入，适用于 AI Agent 自动为工具调用付费 | HTTP 402 质询-响应流程；Charge Intent / Session Intent 两种支付模式；Tempo 区块链 USDC 结算；Stripe SPT 集成；mppx SDK 封装 | [OrcaQubits `stripe-mpp`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/stripe-mpp)（12 个 skill） |
| **WebMCP**（Web Model Context Protocol） | Google、Microsoft、W3C | [webmachinelearning.github.io/webmcp](https://webmachinelearning.github.io/webmcp/)（W3C 草案） | 让现有网站无需后端改造就能被 AI Agent 感知和操作，通过浏览器原生 API 暴露结构化工具 | `navigator.modelContext` 浏览器 API；`registerTool`（声明可被 Agent 调用的操作）；声明式表单 HTML 属性注解；Human-in-the-Loop 确认流程；商品页注册 addToCart/checkout 工具供 Agent 直接调用 | [OrcaQubits `webmcp-browser-agents`](https://github.com/OrcaQubits/agentic-commerce-skills-plugins/tree/main/webmcp-browser-agents)（14 个 skill） |

---

## 附录：来源索引

| Repo | 类型 | 电商 Skill / 工具数量 | 许可证 |
|---|---|---|---|
| [Shopify/Shopify-AI-Toolkit](https://github.com/Shopify/Shopify-AI-Toolkit) | 官方 Skill | 17 个 skill | 不接受 PR |
| [OrcaQubits/agentic-commerce-skills-plugins](https://github.com/OrcaQubits/agentic-commerce-skills-plugins) | Skill + 协议 Plugin | 100+ skill（5 个平台 + 6 个协议） | MIT |
| [40RTY-ai/shopify-admin-skills](https://github.com/40RTY-ai/shopify-admin-skills) | 运营操作型 Skill | 63 个 skill（10 个分类） | MIT |
| [jezweb/claude-skills](https://github.com/jezweb/claude-skills) | 开发型 Skill | ~8 个（Shopify plugin） | MIT |
| [jeffreydebolt/ecom-cfo-skill](https://github.com/jeffreydebolt/ecom-cfo-skill) | 财务诊断 Skill | 1 个 | MIT |
| [takechanman1228/claude-ecom](https://github.com/VoltAgent/awesome-agent-skills) | 数据分析 Skill | 1 个 | — |
| [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 营销 Skill | ~6 个（含电商场景） | MIT |
| [Microck/ordinary-claude-skills](https://github.com/Microck/ordinary-claude-skills) | API 集成 Skill | 1 个 | — |
| [TeamDijon/shopify-rules](https://github.com/TeamDijon/shopify-rules) | 主题开发 Skill | 1 个 | — |
| [mrgoonie/claudekit-skills](https://github.com/mrgoonie/claudekit-skills) | 支付集成 Skill | 1 个 | — |
| [GeLi2001/shopify-mcp](https://github.com/GeLi2001/shopify-mcp) | MCP Server | 31 个工具 | — |
| [apify/apify-mcp-server](https://github.com/apify/apify-mcp-server) | MCP Server | 8000+ Actors | Apache 2.0 |
| [slavpilus/mcp](https://github.com/slavpilus/mcp) | MCP Server | 14 个工具 | — |

---

*最后更新：2026 年 4 月 | 数据来源：各 GitHub repo README 及 SKILL.md 原文*
