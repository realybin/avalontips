# 性能

这里有官方的一些提高性能的建议

[10 Avalonia Performance Tips to Supercharge Your App](https://avaloniaui.net/blog/10-avalonia-performance-tips-to-supercharge-your-app)

[提高性能 | Avalonia Docs](https://docs.avaloniaui.net/zh-Hans/docs/guides/development-guides/improving-performance)

## Android
!!! warning "Android 上为什么帧数低？"
    以下是emmauss的[解答](https://github.com/AvaloniaUI/Avalonia/discussions/17028#discussioncomment-10686250)  
    > 在 Android 上，我们受到 Mono jit 能够提供的性能的限制。由于所有 Android 上的 dotnet 应用程序都受到它的影响，我们几乎无能为力。