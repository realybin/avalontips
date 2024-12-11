# Native Aot Deployment

!!! tips ""
    在阅读本文档之前，请先阅读官方文档 [部署 | Native AOT Deployment](https://docs.avaloniaui.net/zh-Hans/docs/deployment/native-aot)


## 平台/架构限制

以下数据来自官方文档 [Platform/Architecture Restrictions | .NET](https://learn.microsoft.com/dotnet/core/deploying/native-aot/?tabs=windows%2Cnet9plus#platformarchitecture-restrictions)

!!! warning ""
    LoongArch 架构目前不支持Aot

=== ".NET 8"

    | 平台            | 支持的架构  | 注记                      | 
    |---------------|------------|--------------------------|
    | Windows       | x64, Arm64 |                          |
    | Linux         | x64, Arm64 |                          |
    | macOS         | x64, Arm64 |                          |
    | iOS           | Arm64      | 实验性支持                 |
    | iOSSimulator  | x64, Arm64 | 实验性支持                 |
    | tvOS          | Arm64      | 实验性支持                 |
    | tvOSSimulator | x64, Arm64 | 实验性支持                 |
    | MacCatalyst   | x64, Arm64 | 实验性支持                 |
    | Android       | x64, Arm64 | 实验性, 无内置 Java interop |

=== ".NET 9"

    | 平台           | 支持的架构        | 注记                       | 
    |---------------|-----------------|---------------------------|
    | Windows       | x64, Arm64, x86 |                           |
    | Linux         | x64, Arm64, Arm |                           |
    | macOS         | x64, Arm64      |                           |
    | iOS           | Arm64           |                           |
    | iOSSimulator  | x64, Arm64      |                           |
    | tvOS          | Arm64           |                           |
    | tvOSSimulator | x64, Arm64      |                           |
    | MacCatalyst   | x64, Arm64      |                           |
    | Android       | x64, Arm64, Arm | 实验性, 无内置 Java interop |
