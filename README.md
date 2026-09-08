# FrameworkTutorial

FrameworkTutorial 是 SSFramework 的独立教程工程，原 `DemoScene` 名称只描述了其中一张场景，不能表达整个教程工程的用途。它包含可运行的框架章节、代码导航和教学验证，不包含 Outpost 或 NomadWorkshop 的运行时代码。

当前 Unity 资产仍位于 `Assets/Game/DemoScene/`，这是从旧工作区迁移时暂时保留的资产路径；场景与 Prefab 的正式改名将在 Unity Editor 中完成，避免手改序列化引用。

## 依赖边界

- Unity：6000.3.22f1
- Framework：`com.liss.ssframework`
- Framework 以 Git submodule 固定在 `Packages/com.liss.ssframework/`
- 教程程序集暂时保留 `Game.Framework.Demo` 稳定标识，待 Unity Editor 迁移为 `Game.Framework.Tutorial`

FrameworkTutorial 不依赖 Outpost 或 NomadWorkshop。需要展示其它项目时，只使用文档链接或 `Samples~` 示例，不把另一个 Unity 工程纳入当前编译图。

## 分支

`main` 是可跟随教学的稳定版本，`develop` 是章节集成分支，章节改动使用短期 `feature/chapter-*` 分支。发布使用 `vX.Y.Z` Tag，并在 `docs/framework-compatibility.md` 记录 Framework 版本。

## 打开与验证

```text
git submodule update --init --recursive
```

打开根目录后运行 `Assets/Game/DemoScene/Scenes/DemoScene.unity`。章节契约与 PlayMode 验证位于相邻 `Tests` 目录。