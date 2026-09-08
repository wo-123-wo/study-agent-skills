# Study Agent Skills · 学科深潜导师技能包

为 RikkaHub 助手设计的 14 个 Skill，解决四个学习痛点：
只见树木不见森林 / 找不到最资深的人和资源 / 走弯路 / 学不下去。

## 安装
1. RikkaHub → 设置 → 扩展管理 → Skills → `+`
2. 选「从 GitHub 导入」贴本仓库 URL，或「从文件导入」选打包好的 .zip
3. 在目标助手中启用全部 14 个 Skill（enabledSkills）

## 依赖建议
- 模型：强推理长上下文旗舰模型，reasoningLevel = HIGH
- 联网搜索：必开（Exa 优先，用于找一手源/论坛/论文）
- 工作区：新建英文名工作区（如 study）并安装 Rootfs，绑定到该助手
- 记忆：开启，useGlobalMemory = false（每门课隔离）

## 调用关系
study-mentor 是唯一入口（总控路由），其余 13 个由它按阶段调度。

course-intake → terrain-map → veteran-scout → canon-curation → roadmap-planner
                                    ↓                ↓
                              pitfall-radar    source-vetting

执行期：project-ladder / deep-explain / drill-and-review / toolbench-setup
异常期：stuck-doctor
每轮收尾：progress-journal

## 文件产出约定（工作区）
courses/<课程名>/
  contract.md   立项契约
  map.md        全景地图
  mentors.md    师门档案
  library.md    资料分级库
  roadmap.md    里程碑路线
  log.md        学习日志
  projects/     项目复盘

## 硬约束
- 文件夹名必须与 SKILL.md frontmatter 的 name 完全一致
- 主文件名必须是大写 SKILL.md
