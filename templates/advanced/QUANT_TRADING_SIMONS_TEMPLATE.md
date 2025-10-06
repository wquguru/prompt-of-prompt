<!--
1. 本文件是“开源量化项目”标准化模板的“詹姆斯·西蒙斯理念内嵌版”。
用法：替换 {PLACEHOLDER}，并在每节的「西蒙斯对齐」清单中打勾/给出证据。
补充目标：在不改变模板结构的前提下，将数据优先、可证伪、小优势叠加、纪律化执行、持续自动化等理念落实为可操作检查项。

2. 整体目标：基于本文件的格式规范，理解用户给出的源代码路径中的源代码，输出一个文档

3. 细化要求：
   3.a. 文件保存路径为~/Workshop/daily-prompts
   3.b. 文件命名需要为英文，全小写，规范为<项目名>_<日期>.md，如"binance_scalping_20250925.md"
-->

# {PROJECT_NAME} — 量化交易标准化技术文档（西蒙斯理念内嵌版）

> v{DOC_VERSION} · {YYYY-MM-DD} · {LANGS_AND_STACK}

## 0 元信息
- 仓库：{REPO_URL_OR_PATH}
- 运行目标：{RUN_TARGETS}
- 交易场所：{EXCHANGES}
- 关注重点：{FOCUS}
- 参考上下文：{CONTEXT}
- 文档维护者：{DOC_AUTHOR} · {DOC_CONTACT}
- 理念基调（只写一次）：数据先行 · 小优势叠加 · 可证伪 · 自动化与度量 · 风险优先

## 目录
<!-- 渲染器可自动生成 TOC，或手写锚点 -->

---

## 1 概览与要点（Overview）

### 1.1 背景与目标
- 背景：{OVERVIEW_BACKGROUND}
- 目标：{OVERVIEW_GOALS}
- 适用市场/品种：{OVERVIEW_MARKETS}
- Alpha 假设与失效条件：{OVERVIEW_ALPHA_AND_FAILURE}

西蒙斯对齐（勾选并给证据链接）
- [ ] 目标量化为可测指标（如超额年化、IR、t 统计）
- [ ] 假设可被证伪，列出最小失效观测与阈值
- [ ] 优先数据与统计证据，而非主观叙事
- [ ] 假设足够朴素，可组合成小优势叠加

### 1.2 外部依赖总览
- 数据源：{OVERVIEW_DATA_SOURCES}
- 交易所/链上组件：{OVERVIEW_EXCHANGES_ONCHAIN}
- 运行环境（OS/CPU/GPU/内存）：{OVERVIEW_ENV}

西蒙斯对齐
- [ ] 数据源具备溯源与版本戳（时间、供应商、修订）
- [ ] 明确时区/时钟与对齐策略（先对齐再计算）
- [ ] 核心依赖提供最小替代/降级路径

### 1.3 快速结论与注意事项
- 何时适用：{OVERVIEW_WHEN_USE}
- 何时不适用：{OVERVIEW_WHEN_NOT_USE}
- 已知风险：{OVERVIEW_RISKS}

西蒙斯对齐
- [ ] 清晰记录“不要用在”边界与反例
- [ ] 明确容量/滑点/成本支配区

### 1.4 面向初学者
- TL;DR（3-5条）：
  - {OVERVIEW_TLDR_1}
  - {OVERVIEW_TLDR_2}
  - {OVERVIEW_TLDR_3}
- 核心回路（ASCII）：
```
{OVERVIEW_LOOP_ASCII}
```
- 核心回路（Mermaid Flowchart）：
```mermaid
{MERMAID_OVERVIEW_FLOW}
```
- 学习路径与阅读顺序：{OVERVIEW_LEARNING_PATH}

西蒙斯对齐
- [ ] 科学方法闭环：提出→检验→证伪→保留→自动化
- [ ] “工具先行”：复用数据/回测/度量工具优先于个别策略

---

## 2 系统架构说明（Architecture）

### 2.1 架构与模块
- 高层架构图（ASCII/描述）：
```
{ARCH_OVERVIEW_DIAGRAM}
```
- 高层架构图（Mermaid）：
```mermaid
{MERMAID_ARCH_OVERVIEW}
```
- 核心模块：{ARCH_CORE_MODULES}
  - 数据接口：{ARCH_DATA_IFACE}
  - 策略与信号：{ARCH_STRATEGY_SIGNAL}
  - 执行与撮合：{ARCH_EXECUTION_MATCHING}
  - 风控与持仓：{ARCH_RISK_PORTFOLIO}
  - 回测与指标：{ARCH_BACKTEST_METRICS}
  - 监控与告警：{ARCH_OBSERVABILITY}

西蒙斯对齐
- [ ] 模块边界清晰、可替换（信号↔执行↔风控解耦）
- [ ] 工具化/平台化优先（实验、特征、回测统一接口）
- [ ] 数据流先于控制流设计（只读→变更隔离）

### 2.2 数据流与控制流
- 数据流：{ARCH_DATA_FLOW}
- 控制流：{ARCH_CONTROL_FLOW}
- 关键事件/回调：{ARCH_EVENTS}

西蒙斯对齐
- [ ] 延迟与缓冲策略可度量（每段 P50/P99）
- [ ] 事件可重放（为调试/归因）

### 2.3 关键函数速查表（文件:行）

| 职责 | 位置 | 函数/类 | 备注 |
|---|---|---|---|
| {FUNC_DESC_1} | {FILE_1}:{LINE_1} | {SYMBOL_1} | {NOTE_1} |
| {FUNC_DESC_2} | {FILE_2}:{LINE_2} | {SYMBOL_2} | {NOTE_2} |
| {FUNC_DESC_3} | {FILE_3}:{LINE_3} | {SYMBOL_3} | {NOTE_3} |

### 2.4 配置到行为映射
- 示例参数：{CFG_PARAM_EXAMPLE}
- 影响路径：{CFG_TO_BEHAVIOR_PATH}

西蒙斯对齐
- [ ] 任一参数变化可追踪到指标变化（可审计）

### 2.5 面向初学者
- 下单时序图（文字/ASCII）：
```
{ORDER_SEQUENCE_ASCII}
```

- 下单时序图（Mermaid Sequence）：
```mermaid
{MERMAID_ORDER_SEQUENCE}
```

---

## 3 策略与算法规范（Strategy Spec）

### 3.1 交易假设与指标
- 假设来源：{STRAT_HYPOTHESES}
- 特征工程：{STRAT_FEATURES}
- 指标/过滤：{STRAT_INDICATORS_FILTERS}

西蒙斯对齐
- [ ] 假设来源于数据统计与可重复现象
- [ ] 指标与标签严格时间隔离（无前视）
- [ ] 尽量选择简单稳健特征，偏好正交/弱相关

### 3.2 进出场逻辑（伪代码）
```pseudo
{STRAT_PSEUDOCODE}
```

西蒙斯对齐
- [ ] 将“人读得懂”的伪代码同步到“机可复现实验”

### 3.3 资金管理与风控
- 头寸 sizing：{STRAT_SIZING}
- 止损/止盈：{STRAT_STOP_TAKE}
- 限频/限额：{STRAT_RATE_LIMITS}
- 风控状态机：{STRAT_RISK_STATE_MACHINE}

西蒙斯对齐
- [ ] 小优势叠加、单信号不过度下注（Kelly 折扣/风格中性）
- [ ] 组合去相关（目标相关矩阵、波动平价/风险预算）
- [ ] 止损/回撤硬阈值可自动触发与回退

### 3.4 关键超参

| 名称 | 默认值 | 单位 | 范围 | 敏感性 | 备注 |
|---|---|---|---|---|---|
| {HP_1_NAME} | {HP_1_DEFAULT} | {HP_1_UNIT} | {HP_1_RANGE} | {HP_1_SENS} | {HP_1_NOTE} |
| {HP_2_NAME} | {HP_2_DEFAULT} | {HP_2_UNIT} | {HP_2_RANGE} | {HP_2_SENS} | {HP_2_NOTE} |

西蒙斯对齐
- [ ] 超参自由度有限且有先验（防过拟合）
- [ ] 对超参做灵敏度与稳健区间报告

### 3.5 失效与鲁棒性
- 失效场景：{STRAT_FAILURE_MODES}
- 对手方反制：{STRAT_ADVERSARIAL}
- 提升建议：{STRAT_ROBUSTNESS}

西蒙斯对齐
- [ ] 明确非平稳/结构突变应对（退化策略/停机）
- [ ] 将对手方反制视为常态（报价/撮合/MEV）

### 3.6 面向初学者
- 决策树/状态机（ASCII）：
```
{STRAT_STATE_MACHINE_ASCII}
```

- 策略状态机（Mermaid State）：
```mermaid
{MERMAID_STRAT_STATE}
```
- 典型样例：{STRAT_EXAMPLE_IO}
- 代码映射（文件:行清单）：{STRAT_CODE_MAPPING}
- 最小调参实验：{STRAT_MIN_TUNING_EXP}

### 3.7 信号有效性与检验（轻量）
- 交叉验证（最小可用）：{STRAT_TS_CV_SCHEME}（Walk-forward + Embargo 可选）
- 置换对照（任选其一）：{STRAT_PLACEBO_PERM_TESTS}（打乱时间或标签）
- 泄露自检：{STRAT_LEAKAGE_AUDIT}（仅检查对齐/滞后/前视）
- 稳健性维度（≤3项）：{STRAT_ROBUST_DIMENSIONS}（如时段/费率/撮合）

西蒙斯对齐
- [ ] 使用时间序列 CV（封禁期/组合清洗）
- [ ] 显式纳入交易成本与冲击
- [ ] 报告t统计、IR、命中率与持有期分布

### 3.8 市场状态识别（可选）
- 简单划分：{STRAT_REGIME_DEFS}（高/低波动、趋势/震荡）
- 切换规则：{STRAT_REGIME_SWITCH_RULES}（基于 ATR/RSI 的阈值）
- 策略调度（可选）：{STRAT_REGIME_POLICY}（启停/权重切换）

西蒙斯对齐
- [ ] 避免“事后最优切分”；仅用上线前可得的信息

### 3.9 容量与滑点（轻量）
- 经验滑点曲线：{STRAT_IMPACT_MODELS}（成交量占比 vs. 滑点）
- 成交率记录：{STRAT_FILL_RATE_LATENCY_SENS}（按品种/时段统计）
- 放量计划：{STRAT_SCALE_UP_PLAN}（分档资金上限）

西蒙斯对齐
- [ ] 容量是策略定义的一部分（给出函数/曲线）
- [ ] 明确“上线阈值”和“放量步进”

### 3.10 资金管理限额（最小集）
- 限额维度：{STRAT_LIMIT_DIMENSIONS}（单笔/单品种/账户总额）
- 限额表：

| 维度 | 指标 | 硬限 | 软限 | 动态调整规则 | 备注 |
|---|---|---|---|---|---|
| {DIM_1} | {METRIC_1} | {HARD_1} | {SOFT_1} | {ADJUST_RULE_1} | {NOTE_1} |

### 3.11 超参灵敏度与稳健化
- 灵敏度热力图/等高线：{HP_SENS_HEATMAP_ARTIFACT}
- 稳健区间与建议步长：{HP_SENS_GUIDE}
- 正则化/集成/Dropout 等稳健化：{HP_ROBUST_TECHNIQUES}

西蒙斯对齐
- [ ] 采用集成/装袋/去相关来叠加小优势
- [ ] 对自由度进行惩罚与报告（AIC/BIC/有效自由度）

### 3.12 实盘灰度与回退（轻量）
- 上线门槛：{ROLL_OUT_CRITERIA}（回测指标达标+1天纸上交易）
- 灰度放量：{ROLL_OUT_GRADUAL}（1%→5%→20% 资金）
- 快速回退：{ROLLBACK_KILL_SWITCH}（净值跌幅/连续亏损触发）
- 配置留痕：{ROLL_OUT_VERSION_CONFIG}（用 Git 记录参数）

西蒙斯对齐
- [ ] 以实验为单位推进，设定明确终止标准（优/劣）

---

## 4 交易所与连接器适配（Exchanges & Connectors）

### 4.1 共性
- 价格来源：{EX_COMMON_PRICE_SOURCE}
- 时钟/时区：{EX_COMMON_CLOCK_TZ}
- 费率/滑点：{EX_COMMON_FEES_SLIPPAGE}
- 延迟/重连：{EX_COMMON_LATENCY_RECONNECT}
- 幂等/去重：{EX_COMMON_IDEMPOTENCY_DEDUP}

西蒙斯对齐
- [ ] 精确定义“成交价格语义”（标记价/中价/最优价）
- [ ] 关键路径具备重试与去重键

### 4.2 Binance（CEX）
- API（REST/WebSocket）：{BINANCE_APIS}
- 限频与签名：{BINANCE_RATELIMIT_SIGNING}
- 订单类型与精度：{BINANCE_ORDER_TYPES_PRECISION}
- 账户/保证金模式：{BINANCE_MARGIN_MODE}
- 只减仓/强平：{BINANCE_REDUCE_ONLY_LIQ}
- 对账与补单：{BINANCE_RECONCILIATION}

### 4.3 Hyperliquid（去中心化永续）
- 签名与交易时序：{HL_SIGNING_TIMING}
- 资金费率/标记价：{HL_FUNDING_MARKPRICE}
- 只减仓与风险参数：{HL_REDUCE_ONLY_RISK}

### 4.4 Uniswap v3（AMM）
- Tick/刻度与价格映射：{UNI_TICK_PRICE}
- 集中流动性与手续费档：{UNI_LIQUIDITY_FEE_TIER}
- TWAP/价格保护：{UNI_TWAP_GUARDS}

### 4.5 Jupiter（Solana 聚合路由）
- 路由与最优报价：{JUP_ROUTING}
- 账户与打包：{JUP_ACCOUNTS_BUNDLE}
- MEV 风险与重试：{JUP_MEV_RETRY}

---

## 5 数据、回测与指标（Data & Backtest）

### 5.1 数据源与格式
- 行情数据：{DATA_MARKET}
- 账户/订单数据：{DATA_ACCOUNT_ORDER}
- 文件/表结构与路径：{DATA_SCHEMA_PATHS}

- 数据模型/产物关系（Mermaid ER/Class）：
```mermaid
{MERMAID_DATA_MODEL}
```

西蒙斯对齐
- [ ] 数据清洗规则版本化（缺失、异常、复权、对齐）
- [ ] 每条数据可追溯（来源、时间、修订历史）

### 5.2 回测设置
- 时段与频率：{BT_RANGE_FREQ}
- 成本模型（fee/slippage/tax）：{BT_COST_MODEL}
- 撮合近似：{BT_MATCHING_MODEL}
- 随机种子与可复现：{BT_SEED_REPRO}

西蒙斯对齐
- [ ] 成本模型保守、包含冲击函数
- [ ] 撮合近似经过样本外校准
- [ ] 任意回测可一键复现（代码+配置+数据指纹）

### 5.3 指标与产物
- 指标列表：{BT_METRICS_LIST}
- 产物目录：{BT_ARTIFACTS_DIR}
- 输出文件：{BT_OUTPUT_FILES}

西蒙斯对齐
- [ ] 产物包含回放与归因（贡献度、交易对、信号分解）

---

## 6 执行、风控与基础设施（Execution & Infra）

### 6.1 订单与执行器
- 支持订单类型：{EXEC_ORDER_TYPES}
- 执行策略（IOC/FOK/限价/市价）：{EXEC_POLICIES}
- 幂等与重试：{EXEC_IDEMPOTENCY_RETRY}

西蒙斯对齐
- [ ] 执行独立于信号，支持模拟与实盘同构
- [ ] 记录队列位置/重试/撤改用于 TCA

### 6.2 并发与性能
- 并发模型（线程/协程/进程）：{EXEC_CONCURRENCY_MODEL}
- 吞吐/延迟瓶颈：{EXEC_PERF_BOTTLENECKS}
- 指标埋点：{EXEC_METRICS}

西蒙斯对齐
- [ ] 延迟预算有目标、有实测、有回归

### 6.3 可观测性
- 日志级别与结构：{OBS_LOGGING}
- 运行指标：{OBS_RUNTIME_METRICS}
- 告警通道：{OBS_ALERTING}

西蒙斯对齐
- [ ] 指标驱动运维：错误率/延迟/滑点/成交率可视化

### 6.4 拆单与路由（可选，多交易所才需要）
- 单交易所最小实现：{EXEC_CHILD_POLICIES}（限价+超时撤单）
- 可选拆单：{EXEC_CHILD_POLICIES}（TWAP/VWAP/冰山）
- 多交易所路由（可选）：{EXEC_ROUTING_RULES}（最优价/成本/可得性）
- 价格保护：{EXEC_PRICE_GUARDS}（滑点上限/订单过期）

### 6.5 部分成交与重定价
- Cancel/Replace 策略：{EXEC_CR_RULES}（何时撤改、剩余寿命）
- Reduce-Only/只减仓：{EXEC_REDUCE_ONLY_FLOWS}
- 再定价触发：{EXEC_REPRICE_TRIGGERS}（盘口变化/队列位置/延迟）

### 6.6 延迟预算与微结构敏感性
- 延迟预算表：

| 组件 | 预算(ms) | 实测 P50 | 实测 P99 | 备注 |
|---|---:|---:|---:|---|
| Market Data → 策略 | {BUDGET_MD_TO_STRAT} | {P50_1} | {P99_1} | {NOTE_1} |
| 策略 → 下单 | {BUDGET_STRAT_TO_ORDER} | {P50_2} | {P99_2} | {NOTE_2} |
| 下单 → 交易所ACK | {BUDGET_ORDER_ACK} | {P50_3} | {P99_3} | {NOTE_3} |
| ACK → 成交 | {BUDGET_ACK_FILL} | {P50_4} | {P99_4} | {NOTE_4} |

- 微结构敏感性：{EXEC_MICROSTRUCTURE_SENS}（队列位置/刷新频率/撮合近似）

### 6.7 执行质量评估（TCA）
- 基准定义：{TCA_BENCHMARKS}（Mid/Arrival/Decision/TWAP/VWAP）
- 滑点分解：{TCA_SLIPPAGE_DECOMP}（到达/实现/机会成本）
- 成交率/重复下单率：{TCA_FILL_CANCEL_RATES}
- 报表与产物：{TCA_REPORT_ARTIFACTS}

西蒙斯对齐
- [ ] TCA 反馈闭环影响信号与路由权重

### 6.8 保护与熔断
- 预交易检查：{EXEC_PRE_TRADE_CHECKS}（限价/限额/仓位/净敞口/风险状态）
- 交易中保护：{EXEC_INTRA_TRADE_GUARDS}（价格带/速率限制/自成交保护）
- 交易后核对：{EXEC_POST_TRADE_RECON}
- 熔断与回退：{EXEC_CIRCUIT_BREAKERS}（触发阈值/冷却时间/恢复流程）

### 6.9 容错、对账与恢复（轻量）
- 幂等与重放：{EXEC_IDEMPOTENCY_KEYS}（简单去重键）
- 会话与重连：{EXEC_SESSION_RECOVERY}
- 账实对账：{EXEC_LEDGER_RECON}（每日对账单核对）
- 故障演练：{EXEC_CHAOS_TESTS}（手工断网/撤单演练）

---

## 7 部署与运维（Deploy & Ops）

### 7.1 环境与配置
- 环境变量清单：{DEP_ENV_VARS}
- 配置文件：{DEP_CONFIG_FILES}

西蒙斯对齐
- [ ] 配置可审计与不可变打包（Declarative + Hash）

### 7.2 启动与命令
- 本地运行：`{DEP_LOCAL_CMD}`
- 容器化：`{DEP_DOCKER_CMD}`
- 计划任务/守护：{DEP_SCHEDULING}

### 7.3 升级与回滚
- 版本策略：{DEP_VERSIONING}
- 回滚流程：{DEP_ROLLBACK}

西蒙斯对齐
- [ ] 蓝绿/灰度与快速回退路径清晰

### 7.4 部署拓扑（Mermaid）
```mermaid
{MERMAID_DEPLOYMENT}
```

---

## 8 风险、合规与安全（Risk & Compliance）

### 8.1 风险源
- 模型/市场/做市对手：{RISK_MODEL_MARKET_COUNTERPARTY}
- 基础设施/协议：{RISK_INFRA_PROTOCOL}
- 密钥与权限：{RISK_KEYS_PERMS}

西蒙斯对齐
- [ ] 风险预算先于收益目标（最大回撤/日亏/杠杆）

### 8.2 合规模块
- KYC/税务/管辖：{COMPLIANCE_KYC_TAX}
- 日志/报表保留：{COMPLIANCE_RETENTION}
- 敏感数据处理：{COMPLIANCE_SENSITIVE_DATA}

### 8.3 安全清单
- 密钥管理：{SEC_KEY_MGMT}
- 最小权限：{SEC_LEAST_PRIVILEGE}
- 限频/防重放：{SEC_RATELIMIT_REPLAY}
- 依赖与供应链：{SEC_SUPPLY_CHAIN}

### 8.4 威胁模型视图（Mermaid）
```mermaid
{MERMAID_THREAT_MODEL}
```

### 8.5 风险阈值与限额（轻量）
- 关键阈值：{RISK_APPETITE_STATEMENT}（最大回撤、单日亏损、最大杠杆）
- 限额表：{RISK_LIMITS_FRAMEWORK}（单品种/账户/策略上限）
- 升级路径：{RISK_BUDGET_ALLOCATION}（触发阈值→人工确认）

### 8.6 风险监控指标（最小集）
- 实时：{RISK_RT_INDICATORS}（净敞口、持仓、未实现PnL）
- 日频：{RISK_DAILY_INDICATORS}（日收益、回撤、杠杆）
- 告警与处置：{RISK_ALERT_RUNBOOK}（阈值→短信/IM 提醒→手工处置）

### 8.7 故障响应与演练（轻量）
- 联系人清单：{IR_RACI_ONCALL}（2人即可，含电话/IM）
- 响应目标：{IR_SLO}（发现<10m，处理<30m）
- 月度演练：{IR_GAME_DAYS}（断网/交易所不可用）
- 复盘模板：{IR_POSTMORTEM_TEMPLATE}

### 8.8 密钥与机密（轻量实践）
- 存储：{SEC_KMS_HSM}（密码管理器或 `.env` + 加密仓库）
- 轮换：{SEC_ROTATION_REVOCATION}（季度更换/API Key 最短权限）
- 紧急访问：{SEC_BREAK_GLASS}（第二人封存备份）

### 8.9 访问与变更（轻量）
- 账号：{SEC_JIT_ACCESS}（仅交易所与服务器2FA）
- 双人复核：{SEC_CHANGE_CONTROL}（参数/版本变更 PR 或表格）
- 留痕：{SEC_AUDIT_LOG_SCHEMA}（Git 提交信息+变更记录）

### 8.10 依赖与更新管理（轻量）
- 依赖锁定：{SEC_SBOM_SIGNING}（使用 lockfile）
- 漏洞与更新：{SEC_DEP_SCANNING}（按月升级、关注高危告警）
- 构建一致性：{SEC_BUILD_INTEGRITY}（固定镜像/版本）

### 8.11 DeFi 专项风险要点（如适用）
- 预言机与价格操纵：{DEFI_ORACLE_RISK}
- MEV 与夹子：{DEFI_MEV_RISK}
- 协议权限与升级：{DEFI_ADMIN_RISK}

---

## 9 术语与参考（Glossary & References）

### 9.1 术语表
- {GLOSSARY_TERM_1}：{GLOSSARY_DEF_1}
- {GLOSSARY_TERM_2}：{GLOSSARY_DEF_2}

### 9.2 参考资料
- 论文/文档：{REF_PAPERS_DOCS}
- 实现/仓库：{REF_IMPLEMENTATIONS}

附注：本模板的“西蒙斯对齐”条目提炼自公开报道与常识性方法论：以数据和统计为起点、小边际优势的组合与去相关、严格的风险预算与自动化度量。请结合项目实际裁剪。


