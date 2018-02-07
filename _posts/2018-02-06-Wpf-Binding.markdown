---
layout: post
category: "wpf"
title:  "Wpf基础（二）Binding 数据绑定"
tags: [WPF,Binding]
---

WPF通过Binding把数据从.NET对象传递给UI，或从UI传递给.NET对象。CLR对象的每个属性都可以是绑定源，WPF元素也是.NET类的实现，所以WPF元素也可以用作绑定源。

# 绑定模式（Mode） #
首先，MSDN还是最好的老师，网上知识太多太杂，官方资料可以对自己的知识进行系统的整理，[BindingMode 枚举 - MSDN](https://msdn.microsoft.com/zh-cn/library/system.windows.data.bindingmode(v=vs.110).aspx "BindingMode 枚举")。

Binding对象支持源与目标之间的几种绑定模式：

绑定模式|说明|
-|-
一次性（OneTime）|绑定从源指向目标，且仅在应用程序启动时，或数据环境改变时绑定一次。通过这种模式得到数据的快照。只在UI元素初始化时绑定一次。
单向（OneWay）|从绑定源指向目标，但如果目标修改了源不会更新。
双向（TwoWay）|源的修改会更新绑定目标，目标的修改会更新源。
指向源的单向（OneWayToSource）|目标属性改变，源对象也会更新。源对象改变不会影响到目标属性。

还有一种，默认（Default）绑定模式：
> 使用绑定目标的默认 Mode 值。 每个依赖属性的默认值都不同。 通常，用户可编辑的控件属性（如文本框和复选框的控件属性）默认为双向绑定，而其他大多数属性默认为单向绑定。 确定依赖属性绑定在默认情况下是单向还是双向的编程方法是：使用 GetMetadata 获取属性的属性元数据，然后检查 BindsTwoWayByDefault 属性的布尔值。


# 绑定更新 UpdateSourceTrigger #

更新模式|说明
-|-
Explicit|类似手动模式，手动调用UpdateSource方法更新绑定源
LostFocus|在元素失去焦点时更新绑定源
PropertyChanged|在元素属性改变时更新绑定源

默认（Default)绑定模式又是一个特别的情况：
> 大部分控件UpdateSourceTrigger的默认值为PropertyChanged,但是Text控件默认是LostFocus，若使用PropertyChanged可能会导致性能降低。

# 绑定源 Source #
绑定源有几种：

1. ElemenNamet 元素对象
2. Source 指向源对象的引用，即提供数据的对象
3. RelativeSource 设置绑定源的相对位置
4. DataContext 默认绑定源为DataContext，从当前元素开始在逻辑树中向上查找，直到找到第一个非空Datacontext。

Path 绑定源对象属性，绑定源对象为绑定目标时不需要设置或为"."