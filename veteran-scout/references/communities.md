# 资深者与社区起步条目

用途：veteran-scout 的种子清单。每次侦察后把新发现追加进来，长期沉淀成你自己的师门地图。

标注规则：
【A】教科书权威 【B】一线老兵/布道者 【C】社区高信誉 【D】标准与厂商AE 【E】企业实践

---

## 一、电子工程（首发条目）

### 【A】教科书级权威

| 人物 / 著作 | 领域 | 为什么权威 | 怎么用 |
| --- | --- | --- | --- |
| Paul Horowitz & Winfield Hill —《The Art of Electronics》(3rd ed.) | 实用电子学通用 | 几十年被全球实验室与工程师当"电子圣经"，讲的是**能工作的电路**而不是应试推导 | T0 主线常驻参考；配套《AoE X-Chapters》深化；查阅式读，不要从头背 |
| Horowitz & Hill —《Learning the Art of Electronics》 | 动手入门 | AoE 的实验室课程版，逐个实验带你测 | 有面包板/万用表时的最佳 L1 复现来源 |
| Henry W. Ott —《Electromagnetic Compatibility Engineering》 | EMC / 噪声 | EMC 领域奠基级参考，工业界长期引用 | 做板子有干扰问题时的权威依据 |
| Howard Johnson & Martin Graham —《High-Speed Digital Design: A Handbook of Black Magic》 | 高速数字 | 高速信号完整性的经典手册 | 走线/时序/回流路径问题的一手来源 |
| Eric Bogatin —《Signal and Power Integrity – Simplified》 | 信号完整性 | SI/PI 教学体系化，强调物理直觉先于公式 | 从"电路思维"升级到"场与传输线思维"的桥梁 |
| Sedra & Smith / Boylestad | 器件与模电基础 | 高校主流指定教材 | 只作为查询式 T1，不推荐通读 |

### 【B】一线老兵 / 布道者

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

### 【C】社区高信誉源

| 社区 | 适合什么 | 信噪比 | 潜水方式 |
| --- | --- | --- | --- |
| EEVblog Forum | 真实设计/维修/仪器讨论，老兵密度高 | 高 | 按板块潜水（Beginners / Projects / Test Equipment），先看置顶与老帖 |
| Electrical Engineering StackExchange | 具体问题的高质量答案 | 中高 | 按标签 + 高票排序；只信有推导/数据手册引用的答案 |
| r/PrintedCircuitBoard（PCB Review 帖） | 免费的布线评审 | 中高 | 贴出 gerber/原理图求评审，是最快的进步途径之一 |
| r/AskElectronics / r/embedded | 入门与嵌入式实践 | 中 | 提问前先搜，附上你的测量数据 |
| 21ic / 电子工程专辑 / 立创社区（中文） | 国内器件供应、工艺、打样实务 | 中 | 用于查国产料与打样工艺，不用于理论 |
| Hackaday / Hackster | 项目灵感与 L0 火花项目 | 中 | 只取项目点子，不取工程规范 |

### 【D】标准与厂商应用工程（一手源，免费且最被低估）

| 来源 | 内容 | 用法 |
| --- | --- | --- |
| TI Application Notes / TI Precision Labs | 运放、电源、ADC 的系统化课程与 AppNote | 学模拟最强的免费一手源之一，按主题精读 |
| Analog Devices AppNotes / MT-series Tutorials /《Linear Circuit Design Handbook》 | 模拟设计与数据转换 | ADC/DAC、噪声、基准的权威说法 |
| Linear Technology（现 ADI）AppNote AN47（Jim Williams） | 高速放大器技术 + 测量方法 | 经典必读，兼学"怎么测" |
| Microchip / ST / NXP AppNote + Reference Design | MCU 外设、EMC、布板指南 | 做具体芯片前必读对应 AN 与 Hardware Design Guide |
| IPC-2221 / IPC-2141 / IPC-A-610 | PCB 设计与工艺验收标准 | 走线宽度、间距、可制造性的裁判 |
| JEDEC / IEC / CISPR（EN 55032 等） | 器件与 EMC 合规标准 | 判定"能不能过认证"的最终依据 |
| 器件 Datasheet + Errata | 一切的起点 | 铁律：任何器件用前通读电气特性与应用信息章节 + Errata |

### 【E】企业与开源实践

| 来源 | 用法 |
| --- | --- |
| KiCad 官方文档与开源硬件项目（HackRF、Glasgow、开源示波器项目等） | 读真实工程文件：层叠、去耦布局、丝印规范 |
| 大厂公开 Hardware Design Guideline（各 MCU/SoC 厂） | 抄"允许被抄"的规范；理解每条规则背后的物理原因 |
| 打样厂工艺能力表（JLC/PCBWay 等） | 设计前先读，避免设计出做不出来的板 |

### 电子工程：老兵共识（3 人以上交叉后的铁律）
1. **先想回流路径，再画走线**；"地"是参考平面和回流通路，不是等电位点（Hartley / Beeker / Bogatin 一致）。
2. **Datasheet 与 AppNote 是一手源**，教程是二手源；冲突时以前者为准。
3. **不会测量就不算会设计**：万用表→示波器→探头接地弹簧，测量技能与设计技能同权（Jones / Pease / Williams）。
4. **仿真不能替代实测与估算**；先做量级估算，再仿真，最后实测三方对照。
5. **几何决定性能**：高速/混合信号里层叠与空间几何比换更贵的元件更重要（Beeker）。
6. **从可工作的最小系统开始**，逐步加复杂度；不要一次设计一块大板。

### 电子工程：主要分歧（按目标选，不必站队）
- **理论先行 vs 动手先行**：学历路径（考研/科研）偏理论先行；工程就业路径普遍推荐动手先行、按需补理论。
- **2 层板够不够**：低速数字可以；混合信号/高速普遍建议直接上 4 层（成本已很低）。
- **仿真工具介入时机**：一派主张早用仿真建直觉，一派主张先手算与实测防止"仿真依赖症"。

---

## 二、编程 / 软件工程（模板条目）

- 【A】经典著作：SICP、CLRS、《Designing Data-Intensive Applications》(Kleppmann)、《Structure and Interpretation of Computer Programs》
- 【B】老兵：Rob Pike（简洁与工程哲学）、John Carmack（.plan 与工程观）、Kent Beck（TDD）、Martin Fowler（重构）
- 【C】社区：语言官方论坛、Lobsters、对应生态的 GitHub Issue 讨论与 RFC 讨论区
- 【D】一手源：语言规范、RFC、官方文档、编译器/运行时源码注释
- 【E】实践：知名开源项目的 CONTRIBUTING 与代码评审记录

## 三、数学 / 物理（模板条目）

- 【A】经典：Feynman Lectures、Strang《Linear Algebra and Its Applications》、Spivak《Calculus》
- 【B】布道者：3Blue1Brown（建直觉）、Terence Tao（博客中的学习方法论）
- 【C】社区：Math StackExchange、MathOverflow（研究级）
- 【D】一手源：原始论文、arXiv、MIT OCW 等课程讲义
- 【E】实践：把定理用代码实现一遍（数值验证）

---

## 填充规则
- 每类至少 2 人
- 每人必须填"他明确反对的做法"
- 标注年份与可信度（已核实 / 未验证）
- 发现新人物先过 source-vetting 再入册
