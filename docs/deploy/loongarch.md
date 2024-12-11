# LoongArch

!!! info
    本文档仅适用于[新世界](https://areweloongyet.com/docs/old-and-new-worlds)

## SDK

https://areweloongyet.com/project/dotnet

## 相关文档

[移花接木 —— 在其它平台上为 LoongArch 架构打包 .NET 程序](https://driver1998.github.io/posts/dotnet-cross-publish-loongarch/)

## 问题

libHarfBuzzSharp 和 libSkiaSharp 没有 LoongArch 的预编译版本，需要自行编译。

根据官方文档 [Platform/Architecture Restrictions | .NET](https://learn.microsoft.com/dotnet/core/deploying/native-aot/?tabs=windows%2Cnet9plus#platformarchitecture-restrictions)，LoongArch 架构目前不支持 Aot。