# SSFramework Tutorial

这是 SSFramework 的独立章节教程工程，用于把框架 API、模块边界和接入流程放进可运行的教学场景中。它不承担正式游戏玩法。

仓库现已使用 GitHub 名称 `SSFrameworkTutorial`。仓库名称表达教程定位；Unity 资产路径仍暂时保留 `DemoScene`，因为其中包含序列化引用，后续迁移必须通过 Unity Editor/MCP 完成。

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

Framework 升级必须提交新的子模块 gitlink，并运行受影响章节的编译、测试和运行验证。通用安装与升级规则见 [Framework 接入与升级说明](https://github.com/heroliss/SSFramework/blob/main/docs/consuming-framework.md)。

## 直接依赖

- [SSFramework](https://github.com/heroliss/SSFramework)：本教程消费的框架包。
