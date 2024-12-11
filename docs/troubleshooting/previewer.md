# 预览器

!!! tips
    请先查看 [如何使用实时预览 | Avalonia Docs](https://docs.avaloniaui.net/zh-Hans/docs/guides/implementation-guides/ide-support)

## 错误窗口没有显示错误？

### 有参？继承！
检查 [Code-behind](https://docs.avaloniaui.net/zh-Hans/docs/basics/user-interface/code-behind) 中的构造函数是否有参数。

如果有参数，例如：

```csharp title="MainWindow.xaml.cs"
public partial class MainWindow : Window
{
    public MainWindow(MainWindowViewModel viewModel)
    {
        InitializeComponent();
        DataContext = viewModel;
    }
}
```

请做出如下修改


```diff title="MainWindow.xaml.cs" hl_lines="14"
    public partial class MainWindow : Window
    {
--      public MainWindow(MainWindowViewModel viewModel)
--      {
--          InitializeComponent();
--          DataContext = viewModel;
--      }
++      public MainWindow()
++      {
++          InitializeComponent();
++      }

++      public MainWindow(MainWindowViewModel viewModel)
++          : this()
++      {
++          DataContext = viewModel;
++      }
    }
``` 

对于后面代码中的重载构造函数，此处目的是永远不直接调用构造函数，而是依靠依赖注入来自动创建视图实例以及相应的视图模型实例。

我们不能删除默认构造函数，因为这是设计器在使用实时预览器时需要显示的内容。依赖注入框架总是默认使用参数最多的构造函数，因此利用了这一行为。