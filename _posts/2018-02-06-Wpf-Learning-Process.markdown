---
layout: post
category: "wpf"
title:  "Wpf知识点概要"
tags: [wpf,入门,知识点]
---

# 1. 入门需要熟知的知识点 #

 1. Binding
 2. 跨线程操作([Dispatcher](http://blog.csdn.net/lwwl12/article/details/76343771))
 3. 多线程（[异步编程和async/await](http://blog.csdn.net/lwwl12/article/details/76339423)）
 4. template（模板类型【控件模板、数据模板、面板模板】、逻辑树【UI界面的组成元素】、可视化树【逻辑树的扩展版本，将元素分成更小的部分】）
 5. binding（绑定源、绑定模式【default、OneWay、TwoWay、OntTime、OneWayToSource】、触发绑定更新的事件【Default、Explicit(手动BindingExpression.UpdayeSource())、PropertyChange、LostFocus】、）
 6. [trigger](http://blog.csdn.net/lwwl12/article/details/78924703)（4种，属性触发器，数据触发器，事件触发器，多条件触发器）
 6. style
 7. 矩阵操作
 8. lambda
 9. mvvm
 icommand
 convert转换器
 数据绑定Binding
 10. visual、 uielement、 frameworkelement、 control
 11. 用户控件（将控件组合成一个新控件） 自定义控件（重新制造一个控件）
 12. 依赖属性 （优点、定义【属性是类私有字段的封装，wpf中使用属性对依赖属性进行封装】、优先级、继承、附件属性、验证和强制、监听）
 13. MEF（[MEF基础](http://blog.csdn.net/lwwl12/article/details/76855074)、[传送门](http://www.cnblogs.com/yunfeifei/p/3922668.html)、MEF是一个IOC容器，可实现.net程序插件化开发）
 14. prism（一个MVVM框架，依赖IOC容器）
 15. 跨库访问资源（相对地址）
 16. dispatcher
 17. 资源Resources，StaticResource/DynamicResource，静态资源在引用对象初始化时一次性设置完毕；对于动态资源、如果发生了改变则会重新应用资源
 18. 资源字典
 19. 视觉树、逻辑树
 渲染、事件路由、定位资源
 20.  DataSet、DataCommand、DataAdapter
 21. 引用传递 ref out，ref和out都可传出参数，out参数可为空，且在函数中必须赋值
 23. 线程同步、异步、Task
 24. 消息机制、消息泵
 25. abstract、virtual、new、override、sealed
 26. 动画（Timeline、StoryBoard）
 27. 控件缩放、移动、翻转（Thumb）

DPI：单位长度的像素点


# 2. 学习过程 #
1. Application 程序启动
2. Windows 窗体
3. Panel 布局
4. 依赖属性 
5. Binding 绑定
6. 事件机制Event
7. 命令机制Command
8. Resource&Style&Template 资源、样式和模板
9. MVVM入门 (简单MVVM、MVVMLight、Prism)




#########################
最近在网上看到别人写的

###初级工程师###
较强.NET 2.0 基础知识& 愿意学习新技术

解释什么是依赖属性，它和以前的属性有什么不同？为什么在WPF会使用它？

什么是样式（Style）？

什么是模板（template）?

绑定（Binding ）的基础用法

解释这几个类的作用及关系: Visual, UIElement, FrameworkElement, Control

视觉树vs 逻辑树?

属性变更通知(INotifyPropertyChange 和ObservableCollection)

ResourceDictionary

UserControls

事件的三种方式（冒泡、直接、隧道）

###中级工程师###
Routed Events（路由事件） & Commands （命令）

绑定详解（包括绑定到单一属性、实体、集合、值转换、触发机制、验证等）

怎样布局一个漂亮的UI(你们以前的项目是怎么做的？)

WPF和之前的技术交互(WPF/WinForms)

animations 、storyboarding

ClickOnce 部署（优点和缺点）或者是自己通过微软setup/InstallShield+自己的自动更新组件。

样式、主题和触发器

自定义控件

怎样才能工作线程更新UI？
###高级工程师###
什么是attached behavior（附加行为或者附加事件）?

PRISM,CAL & CAG等等框架，是否使用过？你们是怎么用的？没有使用的话，解释一下自己的开发模式和框架。

怎样才能工作线程更新UI？

WPF 3D和动画的应用（是否使用过？用过哪些？）。

Silverlight和WPF的异同。

怎么开发自定义控件？可以简单介绍一下自己开发的控件。

你之前的WPF项目开发流程是怎样的？

三种开发模式（MVVM/MVP/MVC）的理解。

WPF的性能调整（你是怎么优化WPF性能的？）

聊聊你做WPF的一些经验和体会。
