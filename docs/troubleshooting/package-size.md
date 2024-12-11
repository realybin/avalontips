# 包体大小

相关讨论：[Trim down the size of the compiled binary #9217](https://github.com/AvaloniaUI/Avalonia/discussions/9217)

## RuntimeIdentifier
> RID 是运行时标识符的缩写。 RID 值用于标识应用程序运行所在的目标平台。 .NET 包使用它们来表示 NuGet 包中特定于平台的资产。 以下值是 RID 的示例：linux-x64、win-x64 或 osx-x64。 对于具有本机依赖项的包，RID 将指定在其中可以还原包的平台。[^1]

当指定了 RuntimeIdentifier 后，.NET SDK 能够确定目标运行时的具体环境（例如 Windows、Linux 等），这样就可以在发布时只包含与该运行时相关的依赖项，而忽略其他不相关的依赖项。

[^1]: .NET RID Catalog: https://learn.microsoft.com/dotnet/core/rid-catalog
https://learn.microsoft.com/zh-cn/dotnet/core/rid-catalog#using-rids


```xml
<RuntimeIdentifier>android-arm</RuntimeIdentifier>
```

## PublishTrimmed[^2]
[^2]: https://learn.microsoft.com/dotnet/core/deploying/trimming/trim-self-contained

!!! note
    在阅读本节之前，请先阅读官方文档 [部署 | Native AOT Deployment](https://docs.avaloniaui.net/zh-Hans/docs/deployment/native-aot)

!!! note
    - .NET 6 及更高版本完全支持剪裁。 剪裁在 .NET Core 3.1 和 .NET 5 中是一项实验性功能。
    - 剪裁只能用于独立发布的应用程序。
!!! warning
    并非所有项目类型都可以剪裁。 有关详细信息，请参阅[已知剪裁不兼容性](https://learn.microsoft.com/dotnet/core/deploying/trimming/incompatibilities)。

??? tips "WPF 相关"
    - WPF的相关进度 [WPF is not trim-compatible #3811](https://github.com/dotnet/wpf/issues/3811)
    - 一个神奇的项目 支持WPF裁剪、反射 https://github.com/yangzhongke/Zack.DotNetTrimmer
Avalonia支持
```xml
<PublishTrimmed>true</PublishTrimmed>
```
