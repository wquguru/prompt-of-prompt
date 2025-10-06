# 网站文档深度分析提示词模版

## 任务目标

分析{{website_name}}的完整文档体系，深度理解其技术架构、商业模式和融资状况。

## 分析范围

文档入口：{{documentation_entry_url}}
预期文档数量：{{expected_doc_count}}个文档页面

## 分析步骤

### 第一阶段：文档发现与遍历

1. **访问主文档入口**
   - 使用playwright工具访问{{documentation_entry_url}}
   - 识别文档导航结构（侧边栏、目录、链接结构）
   - 提取所有文档页面链接

2. **文档分类映射**
   - 技术文档：API文档、架构说明、开发指南
   - 产品文档：功能介绍、用户指南、使用案例
   - 商业文档：定价、商业模式、合作伙伴
   - 公司文档：关于我们、团队介绍、投资信息

3. **系统性遍历**
   - 按分类顺序访问每个文档页面
   - 提取每页的关键信息和技术细节
   - 记录页面间的关联关系

### 第二阶段：技术架构分析

4. **核心技术栈识别**
   - 后端技术：{{backend_frameworks}}
   - 前端技术：{{frontend_frameworks}}
   - 数据库：{{database_technologies}}
   - 基础设施：{{infrastructure_stack}}
   - 第三方集成：{{third_party_integrations}}

5. **架构模式分析**
   - 系统架构类型：{{architecture_pattern}}
   - 微服务拆分策略
   - 数据流向和处理逻辑
   - 扩展性和性能考量

6. **API设计分析**
   - REST/GraphQL API设计模式
   - 认证授权机制
   - 限流和安全策略
   - 版本管理策略

### 第三阶段：商业模式分析

7. **收入模式识别**
   - 订阅模式：{{subscription_tiers}}
   - 交易佣金：{{commission_structure}}
   - 企业定制：{{enterprise_pricing}}
   - 生态分成：{{ecosystem_revenue}}

8. **目标市场分析**
   - 主要客户群体：{{target_customers}}
   - 市场定位：{{market_positioning}}
   - 竞争优势：{{competitive_advantages}}
   - 增长策略：{{growth_strategy}}

9. **产品策略分析**
   - 核心价值主张：{{value_proposition}}
   - 功能差异化：{{feature_differentiation}}
   - 用户获取成本：{{customer_acquisition}}
   - 客户留存策略：{{retention_strategy}}

### 第四阶段：融资状况分析

10. **融资历史追踪**
    - 融资轮次：{{funding_rounds}}
    - 投资金额：{{investment_amounts}}
    - 投资机构：{{investor_list}}
    - 估值变化：{{valuation_history}}

11. **财务健康度评估**
    - 收入增长趋势：{{revenue_growth}}
    - 盈利能力：{{profitability_status}}
    - 现金流状况：{{cash_flow}}
    - 融资用途：{{fund_usage}}

12. **投资者关系分析**
    - 战略投资者：{{strategic_investors}}
    - 财务投资者：{{financial_investors}}
    - 董事会构成：{{board_composition}}
    - 股权结构：{{ownership_structure}}

## 输出要求

### 技术架构报告
```
## {{website_name}} 技术架构分析

### 整体架构
- 架构模式：{{architecture_summary}}
- 技术栈：{{tech_stack_summary}}
- 核心组件：{{core_components}}

### 关键技术决策
- {{key_tech_decision_1}}
- {{key_tech_decision_2}}
- {{key_tech_decision_3}}

### 扩展性评估
- 当前架构支持的规模：{{scalability_current}}
- 潜在瓶颈：{{potential_bottlenecks}}
- 优化建议：{{optimization_suggestions}}
```

### 商业模式报告
```
## {{website_name}} 商业模式分析

### 收入结构
- 主要收入来源：{{primary_revenue}}
- 收入占比：{{revenue_breakdown}}
- 增长驱动因素：{{growth_drivers}}

### 市场策略
- 目标市场：{{target_market_detail}}
- 竞争策略：{{competitive_strategy}}
- 差异化优势：{{differentiation}}

### 运营模型
- 获客成本：{{cac_analysis}}
- 客户生命周期价值：{{ltv_analysis}}
- 单位经济模型：{{unit_economics}}
```

### 融资状况报告
```
## {{website_name}} 融资分析

### 融资概览
- 总融资金额：{{total_funding}}
- 融资轮次：{{funding_stage}}
- 最新估值：{{latest_valuation}}

### 投资者分析
- 领投机构：{{lead_investors}}
- 战略投资者：{{strategic_investors_detail}}
- 投资逻辑：{{investment_thesis}}

### 财务健康度
- 现金储备：{{cash_reserves}}
- 烧钱率：{{burn_rate}}
- 资金跑道：{{runway}}
```

## 关键信息提取清单

- [ ] 完整遍历所有文档页面
- [ ] 技术架构图和组件关系
- [ ] API接口设计和数据模型
- [ ] 定价策略和商业模式
- [ ] 团队背景和投资者信息
- [ ] 竞争对手和市场地位
- [ ] 增长数据和关键指标
- [ ] 安全合规和风险控制
- [ ] 生态合作和第三方集成
- [ ] 未来发展规划和路线图

## 分析深度要求

每个维度的分析应达到以下深度：
- **技术层面**：深入到具体的技术选型、架构决策理由、性能优化策略
- **商业层面**：分析到具体的收入数字、客户分层、定价策略逻辑
- **融资层面**：追踪到具体投资条款、估值依据、资金使用计划

## 输出格式

最终输出应包含：
1. 执行摘要（500字以内）
2. 详细分析报告（3000-5000字）
3. 关键发现和洞察
4. 风险评估和机会分析
5. 对标竞品分析
6. 投资价值评估（如适用）
