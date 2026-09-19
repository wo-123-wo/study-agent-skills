---
name: veteran-scout
description: 侦察某领域最资深的人、门派与高信噪比社区。当用户问"谁是这个领域的权威/大佬""几十年经验的工程师是怎么学的""行业领头羊的认知""老手在哪交流""该拜谁为师"时使用。输出五类资深者档案卡（含其学习观与明确反对的做法）、共识与分歧交叉表、可长期潜水的社区清单与提问礼仪。
compatibility: 需要联网搜索（Exa / Tavily / Brave 等）以获取真实人物、原帖与年份信息。
allowed-tools: search web_search use_skill
---

# 资深者侦察（Veteran Scout）

## 第一步：先切细分方向
不要笼统地找"电子领域大佬"。电子 ≠ 模拟 ≠ 射频 ≠ 嵌入式 ≠ PCB/EMC ≠ 电源 ≠ 数字IC，
不同细分的师门完全不同。先问/推断细分方向，再开始找人。

## 第二步：五类"资深"必须分开找（别只找网红）

| 类型 | 定义 | 找法关键词 |
| --- | --- | --- |
| A 教科书级权威 | 写出被全行业指定的经典著作 | classic textbook + 领域、被引最多、大学指定教材 |
| B 一线老兵/布道者 | 20-40 年从业，有公开踩坑史 | 40 years experience、conference keynote、常年答疑 |
| C 社区高信誉者 | 论坛/StackExchange 高分老人 | 高票答主、版主、邮件列表老人 |
| D 标准与厂商应用工程师 | 写 AppNote / 设计指南 / 标准 | application note、design guide、标准组织 |
| E 领头企业实践 | 公开的设计规范与工程博客 | 大厂硬件/工程规范、开源项目维护者 |

各类找 2-3 人/源。

## 第三步：人物档案卡（每人一张）

```
姓名 / ID：
身份与年限：
为什么权威：（代表作 / 岗位 / 被谁引用 / 社区声望，必须可核查）
他的学习观：（原话或转述 + 出处 + 年份）
他推荐的入门顺序：
他明确反对的做法：            ← 最值钱的一栏，必须填
在哪能持续跟他学：（书 / 频道 / 论坛 / 讲座 / 邮件列表）
可信度：已核实 / 未验证
```

## 第四步：共识与分歧交叉表
拿 3 位以上老兵的说法做交叉：
- **共识项** → 升级为铁律（写进 map.md 和 pitfall-radar）
- **分歧项** → 标注"流派差异"，并说明各自适用场景，让用户按自己的目标选
- **反直觉项** → 单独列出（这些是新手最容易踩的坑）

## 第五步：社区潜水指南
给 3-5 个高信噪比社区，每个写：

```
社区名 | 适合什么问题 | 信噪比评价 | 潜水方式 | 提问礼仪
```

提问礼仪示例（硬件）：先搜 5 年内老帖 → 贴出原理图片段 + 示波器截图 + 你已试过什么 →
说明你的推断 → 再问；禁止"求大佬帮我看看"。

## 输出与存档
写入 courses/<课程名>/mentors.md；把"明确反对的做法"整段传给 pitfall-radar；
把人物代表作传给 canon-curation 作为 T0 候选。

## 铁律
- 每个人物必须给出**可核查凭据**；给不出就标"未验证"，不得包装成权威。
- 优先英文一手源（论坛原帖、大会演讲、AppNote、标准文本）；中文二手源仅作补充。
- 短视频平台爆款内容不作为权威来源，只能标为"入门情绪激活器"。
- 明确区分：**教得好的人 ≠ 做得好的人**。两类都要，但用途不同（前者用于入门，后者用于判断力）。
- 注明年份：技术类观点 10 年前和今天可能相反。
- 已故的传奇工程师同样有效（其 AppNote 与著作往往是最好的一手源）。

---

# 附录：电子工程起步条目（侦察时直接采用并核实更新）

## 【A】教科书级权威

| 人物 / 著作 | 领域 | 为什么权威 | 怎么用 |
| --- | --- | --- | --- |
| Paul Horowitz & Winfield Hill —《The Art of Electronics》(3rd ed.) | 实用电子学通用 | 几十年被全球实验室与工程师当"电子圣经"，讲的是**能工作的电路**而不是应试推导 | T0 主线常驻参考；配套《AoE X-Chapters》深化；查阅式读，不要从头背 |
| Horowitz & Hill —《Learning the Art of Electronics》 | 动手入门 | AoE 的实验室课程版，逐个实验带你测 | 有面包板/万用表时的最佳 L1 复现来源 |
| Henry W. Ott —《Electromagnetic Compatibility Engineering》 | EMC / 噪声 | EMC 领域奠基级参考，工业界长期引用 | 做板子有干扰问题时的权威依据 |
| Howard Johnson & Martin Graham —《High-Speed Digital Design: A Handbook of Black Magic》 | 高速数字 | 高速信号完整性的经典手册 | 走线/时序/回流路径问题的一手来源 |
| Eric Bogatin —《Signal and Power Integrity – Simplified》 | 信号完整性 | SI/PI 教学体系化，强调物理直觉先于公式 | 从"电路思维"升级到"场与传输线思维"的桥梁 |
| Sedra & Smith / Boylestad | 器件与模电基础 | 高校主流指定教材 | 只作为查询式 T1，不推荐通读 |

## 【B】一线老兵 / 布道者

| 人物 | 身份 | 核心贡献 | 他明确反对的做法（要点） |
| --- | --- | --- | --- |
| Dave Jones（EEVblog） | 澳洲资深电子设计工程师，20 年以上，YouTube 与论坛创办者 | 拆机、量测、设计实录、Fundamentals Friday 系列 | 反对纸上谈兵；反对不看数据手册就用器件；反对新手一上手就买顶级仪器 |
| Rick Hartley | 50 年以上 PCB 设计与 EMI 老兵，IPC 讲师 | 名讲《How to Achieve Proper Grounding》（Altium，约 140 分钟），把"地"讲成"参考平面/回流路径" | 反对星形接地/割地平面式民间口诀；反对把 GND 当电位而不当回流路径 |
| Eric Bogatin | 信号完整性教授/布道者 | 用测量与直觉教 SI/PI，主张"先想物理再算公式" | 反对不做估算就仿真；反对迷信经验法则而不问适用条件 |
| Dan Beeker | NXP 资深应用工程师，EMC/场论布道者 | 主题演讲《Electromagnetic Fields for Normal Folks》/《It's All About the Space!》，用"能量在空间中传播"重构 PCB 认知 | 反对只用集中参数电路思维做高速板；反对"元件决定一切、几何无关"的观念 |
| Robert Feranec（FEDEVEL） | 硬件设计工程师，长期做深度访谈 | 与 Hartley / Bogatin / Beeker 的长访谈，是"听老兵怎么想"的富矿 | 反对跳过原理图评审直接布线 |
| Phil Salmony（Phil's Lab） | 嵌入式硬件工程师 | 从零到 4 层板的完整实战教程（STM32/混合信号/EMI） | 反对新手用 2 层板做混合信号；反对不做 DFM 检查就投板 |
| Bob Pease（已故） | NSC 传奇模拟工程师 | 《Troubleshooting Analog Circuits》、专栏 What's All This ... Stuff, Anyhow? | 反对盲信仿真（仿真不能替代思考和实测）；反对不做故障排查训练 |
| Jim Williams（已故） | Linear Tech 传奇模拟工程师 | Linear AppNote 系列（AN47 等），把 AppNote 写成教科书 | 反对脱离实测的纸面设计；反对忽视测量本身的误差 |
| Michael Ossmann | RF/SDR 硬件（HackRF 作者） | Simple RF Circuit Design 系列讲座 | 反对认为 RF 必须先学完全部电磁场理论才能动手 |

## 【C】社区高信誉源

| 社区 | 适合什么 | 信噪比 | 潜水方式 |
| --- | --- | --- | --- |
| EEVblog Forum | 真实设计/维修/仪器讨论，老兵密度高 | 高 | 按板块潜水（Beginners / Projects / Test Equipment），先看置顶与老帖 |
| Electrical Engineering StackExchange | 具体问题的高质量答案 | 中高 | 按标签 + 高票排序；只信有推导/数据手册引用的答案 |
| r/PrintedCircuitBoard（PCB Review 帖） | 免费的布线评审 | 中高 | 贴出 gerber/原理图求评审，是最快的进步途径之一 |
| r/AskElectronics / r/embedded | 入门与嵌入式实践 | 中 | 提问前先搜，附上你的测量数据 |
| 21ic / 电子工程专辑 / 立创社区（中文） | 国内器件供应、工艺、打样实务 | 中 | 用于查国产料与打样工艺，不用于理论 |
| Hackaday / Hackster | 项目灵感与 L0 火花项目 | 中 | 只取项目点子，不取工程规范 |

## 【D】标准与厂商应用工程（一手源，免费且最被低估）

| 来源 | 内容 | 用法 |
| --- | --- | --- |
| TI Application Notes / TI Precision Labs | 运放、电源、ADC 的系统化课程与 AppNote | 学模拟最强的免费一手源之一，按主题精读 |
| Analog Devices AppNotes / MT-series Tutorials /《Linear Circuit Design Handbook》 | 模拟设计与数据转换 | ADC/DAC、噪声、基准的权威说法 |
| Linear Technology（现 ADI）AppNote AN47（Jim Williams） | 高速放大器技术 + 测量方法 | 经典必读，兼学"怎么测" |
| Microchip / ST / NXP AppNote + Reference Design | MCU 外设、EMC、布板指南 | 做具体芯片前必读对应 AN 与 Hardware Design Guide |
| IPC-2221 / IPC-2141 / IPC-A-610 | PCB 设计与工艺验收标准 | 走线宽度、间距、可制造性的裁判 |
| JEDEC / IEC / CISPR（EN 55032 等） | 器件与 EMC 合规标准 | 判定"能不能过认证"的最终依据 |
| 器件 Datasheet + Errata | 一切的起点 | 任何器件用前通读电气特性与应用信息章节 + Errata |

## 【E】企业与开源实践

| 来源 | 用法 |
| --- | --- |
| KiCad 官方文档与开源硬件项目（HackRF、Glasgow、开源示波器项目等） | 读真实工程文件：层叠、去耦布局、丝印规范 |
| 大厂公开 Hardware Design Guideline（各 MCU/SoC 厂） | 抄"允许被抄"的规范；理解每条规则背后的物理原因 |
| 打样厂工艺能力表（JLC/PCBWay 等） | 设计前先读，避免设计出做不出来的板 |

## 老兵共识（3 人以上交叉后的铁律）
1. **先想回流路径，再画走线**；"地"是参考平面和回流通路，不是等电位点（Hartley / Beeker / Bogatin 一致）。
2. **Datasheet 与 AppNote 是一手源**，教程是二手源；冲突时以前者为准。
3. **不会测量就不算会设计**：万用表→示波器→探头接地弹簧，测量技能与设计技能同权（Jones / Pease / Williams）。
4. **仿真不能替代实测与估算**；先做量级估算，再仿真，最后实测三方对照。
5. **几何决定性能**：高速/混合信号里层叠与空间几何比换更贵的元件更重要（Beeker）。
6. **从可工作的最小系统开始**，逐步加复杂度；不要一次设计一块大板。

## 主要分歧（按目标选，不必站队）
- **理论先行 vs 动手先行**：学历路径（考研/科研）偏理论先行；工程就业路径普遍推荐动手先行、按需补理论。
- **2 层板够不够**：低速数字可以；混合信号/高速普遍建议直接上 4 层（成本已很低）。
- **仿真工具介入时机**：一派主张早用仿真建直觉，一派主张先手算与实测防止"仿真依赖症"。

## 其它学科扩展时的填充规则
- 每类至少 2 人；每人必须填"他明确反对的做法"；标注年份与可信度
- 编程参考：SICP / CLRS / Kleppmann；Rob Pike、John Carmack、Kent Beck；语言规范与 RFC
- 数学物理参考：Feynman Lectures、Strang、Spivak；3Blue1Brown、Terence Tao；Math StackExchange、arXiv、MIT OCW
- 发现新人物先过 source-vetting 再入册
