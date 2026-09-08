# FrameworkTutorial 协作入口

本仓库只维护 SSFramework 教程工程。Framework 源码来自 `Packages/com.liss.ssframework/` 子仓库；Outpost 与 NomadWorkshop 不进入本工程编译图。

- 教程代码：`Assets/Game/DemoScene/`
- Framework 包 ID：`com.liss.ssframework`
- 场景、Prefab 和程序集标识迁移必须通过 Unity Editor/MCP 完成，不能手改 YAML。
- 教学章节引用 Framework 源码时使用 Package-aware 路径，不恢复 `Assets/Game/Framework` 假设。