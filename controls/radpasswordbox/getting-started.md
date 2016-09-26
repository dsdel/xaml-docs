---
title: Getting Started
page_title: Getting Started
description: Getting Started
slug: radpasswordbox-getting-started
tags: getting,started
published: True
position: 1
---

# Getting Started

This tutorial will walk you through the creation of a sample application that contains __RadPasswordBox__.

* [Assembly References](#assembly-references)
* [Adding RadPasswordBox to the Project](#adding-radpasswordbox-to-the-project)
* [Setting Watermark](#setting-watermark)

## Assembly References

In order to use the __RadPasswordBox__ control in your projects, you have to add references to the following assembly:			

* __Telerik.Windows.Controls__

## Adding RadPasswordBox to the Project

Before proceeding with adding __RadPasswordBox__ to your project, make sure the required assembly references are added to the project. 

You can add __RadPasswordBox__ manually by writing the XAML code in __Example 1__. You can also add the control by dragging it from the Visual Studio Toolbox and dropping it over the XAML view.

#### __[XAML] Example 1: Adding RadPasswordBox in XAML__

{{region passwordbox-getting-started_0}}
	<telerik:RadPasswordBox Width="150" />
{{endregion}}

>In order to use __RadPasswordBox__ in XAML you have to add the namespace declaration shown in __Example 2__:
>#### __[XAML] Example 2: Declaring Telerik Namespace__
>{{region telerik-schemas}}
>    xmlns:telerik="http://schemas.telerik.com/2008/xaml/presentation"
>{{endregion}}

If you run the application you will see the PasswordBox as illustrated in __Figure 1__. 

#### __Figure 1: RadPasswordBox generated by the code in Example 1__

![](images/RadPasswordBox_GettingStarted_0.png)

## Setting Watermark

When RadPasswordBox is empty and not focused, Watermark content can be shown. __Example 2__ demonstrates how to set Watermark text.

#### __[XAML] Example 2: Setting a watermark__

{{region passwordbox-getting-started_1}}
	<telerik:RadPasswordBox Width="150" WatermarkContent="enter a password" />
{{endregion}}

__Figure 2__ shows the result.

#### __Figure 2: RadPasswordBoxBox with Watermark set__

![](images/RadPasswordBox_GettingStarted_1.png)

## See Also

 * [Overview]({%slug radpasswordbox-overview%})

 * [Visual Structure]({%slug radpasswordbox-visual-structure%})