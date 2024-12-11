# 安装
## 选择开发工具

!!! tips "为什么预览器没有正常工作？"
    请参阅 [预览器](../troubleshooting/previewer.md)

!!! info ""
    目前 Avalonia 官方没有推出设计器（你可能想要类似于 Visual Studio WPF 设计器的功能），官方目前正在开发中，详情查看 [Request for feedback - Avalonia Accelerate 🚀](https://github.com/AvaloniaUI/Avalonia/discussions/16997)。
    TL;DR: 需要一小笔费用才能使用 Avalonia Accelerate，付费也是对开源工作的保护和支持。
*[TL;DR]: Too Long; Don't Read 太长不看
### JetBrains Rider

自 2023.3 版本开始 JetBrains Rider 内置支持 Avalonia XAML

建议安装适用于Avalonia开发的Rider插件 [AvaloniaRider](https://plugins.jetbrains.com/plugin/14839-avaloniarider/ "AvaloniaRider 插件主页") 

### Visual Studio

如果您正在使用 Visual Studio 开发 Avalonia，您应该安装 [Avalonia for Visual Studio](https://marketplace.visualstudio.com/items?itemName=AvaloniaTeam.AvaloniaVS) 扩展。

- 在 Visual Studio 中，点击**扩展**菜单上的**管理扩展**
- 在**搜索框**中，输入"Avalonia"
- 点击**下载**并按照说明进行操作（您需要关闭Visual Studio以完成安装）

!!! tips ""
    考虑到部分地区的网络环境，你可能无法在 Visual Studio 中直接安装 Avalonia for Visual Studio 扩展。你可以通过 [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=AvaloniaTeam.AvaloniaVS) 下载 `.vsix` 文件，然后在 Visual Studio 中通过 `扩展` -> `管理扩展` -> `从文件安装` 安装。

## 配置模板

在安装模板前，请确保你已[正确安装 .NET SDK](https://learn.microsoft.com/dotnet/core/install/windows)

### 安装模板

要安装 [Avalonia 模板](https://github.com/AvaloniaUI/avalonia-dotnet-templates)，请运行以下命令：

```shell
dotnet new install Avalonia.Templates
```
!!! note
    对于 .NET 6.0 及更早版本，请将`install`替换为`--install`

### 更新模板

如果以前安装过模板，但想安装最新版本，可以使用 [dotnet new update](https://learn.microsoft.com/dotnet/core/tools/dotnet-new-update) 更新已安装的模板。

```shell
dotnet new update
```

### 卸载模板

```shell
dotnet new uninstall Avalonia.Templates
```