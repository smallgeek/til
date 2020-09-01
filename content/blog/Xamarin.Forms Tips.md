---
date: "2020-09-01"
title: "Xamarin.Forms Tips"
---

## Android の TabbedPage のタブを下側に表示する

Android ではデフォルトのタブが画面上側に表示される。
これを下側に表示するには以下の設定を追加する。

```cs
using Xamarin.Forms;

namespace XFSample.Views
{
    public partial class MainPage : TabbedPage
    {
        public MainPage()
        {
            InitializeComponent();

            // ToolbarPlacement で下側に移動させる
            Xamarin.Forms.PlatformConfiguration.AndroidSpecific.TabbedPage.SetToolbarPlacement(
                this, Xamarin.Forms.PlatformConfiguration.AndroidSpecific.ToolbarPlacement.Bottom);
        }
    }
}
```

[Bottom navigation - Material Design](https://material.io/components/bottom-navigation)
