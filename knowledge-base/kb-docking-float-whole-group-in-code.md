---
title: How to Float a PaneGroup in Code-Behind
description: This article demonstrates how to float a RadPaneGroup via code.
type: how-to
page_title: Undock a Whole PaneGroup Programmatically
slug: kb-docking-float-whole-group-in-code
position: 0
tags: docking, float, radpanegroup, code, programmatically, undock
ticketid: 1479470
res_type: kb
---

## Environment
<table>
	<tr>
		<td>Product</td>
		<td>RadDocking for WPF</td>
	</tr>
</table>

## Description

How to undock a RadPaneGroup programmatically.

## Solution

To achieve this requirement you can create the following helper method.

#### __[C#] Example 1: Create the helper method to float a RadPaneGroup__
    {{region cs-kb-docking-float-whole-group-in-code-1}}
        public void FloatGroup(RadPaneGroup paneGroup)
        {
            var panes = paneGroup.EnumeratePanes().ToList();
            var firstPane = panes[0];

            firstPane.MakeFloatingDockable();
            for (var i = 1; i < panes.Count(); i++)
            {
                panes[i].RemoveFromParent();
                firstPane.PaneGroup.AddItem(panes[i], DockPosition.Center);
            }
        }
    {{endregion}}

You can then use this method to undock any RadPaneGroup.

#### __[C#] Example 2: Use the FloatGroup helper method__
    {{region cs-kb-docking-float-whole-group-in-code-1}}
        this.FloatGroup(this.paneGroup1);
    {{endregion}}

## See Also
* [Docked/Floating Panes]({%slug raddocking-features-panes-docked-floating-panes%})