# SSFramework Tutorial

这是 SSFramework 的独立章节教程工程，用于把框架 API、模块边界和接入流程放进可运行的教学场景中。它不包含 Outpost 或 NomadWorkshop 的运行时代码，也不承担正式游戏玩法。

仓库当前 GitHub 名称仍为 `FrameworkTutorial`；`SSFrameworkTutorial` 更能表达它与框架的关系，是建议的正式名称。仓库远端改名需要在 GitHub 设置中单独完成，当前本地目录、远端 URL 和 Unity 资产路径保持不变。

## 当前资产与兼容边界

- Unity：`6000.3.22f1`。
- Framework：`Packages/com.liss.ssframework` Git submodule。
- 教程资产暂时位于 `Assets/Game/DemoScene/`，因为路径包含 Unity 序列化引用；正式改为 `Tutorial` 时必须通过 Unity Editor/MCP 迁移，不能手改场景或 Prefab YAML。
- 教程程序集暂时保留 `Game.Framework.Demo` 标识，待资产迁移与消费方验证完成后再改为 `Game.Framework.Tutorial`。

## 开始使用

```powershell
git submodule update --init --recursive
```

用 Unity Hub 打开仓库根目录，再运行 `Assets/Game/DemoScene/Scenes/DemoScene.unity`。章节说明和测试位于相邻的 `Documentation~` 与 `Tests` 目录；进入章节前先阅读仓库内的 `AGENTS.md`。

## 分支与 Framework 同步

- `main`：可跟随教学的稳定线。
- `develop`：章节集成线。
- `feature/chapter-*`：短期章节开发分支。
- `vX.Y.Z`：教程版本标签。

Framework 升级必须提交新的子模块 gitlink，并运行受影响章节的编译、测试和运行验证。完整的 SHA/tag 同步流程见 [SSFramework 仓库集成说明](https://github.com/heroliss/SSFramework/blob/main/docs/repository-integration.md)。

## 相关仓库

- [SSFramework](https://github.com/heroliss/SSFramework)：被教程消费的框架包。
- [Outpost](https://github.com/heroliss/Outpost)：独立教程游戏。
- [NomadWorkshop](https://github.com/heroliss/NomadWorkshop)：独立开发中的正式游戏。
