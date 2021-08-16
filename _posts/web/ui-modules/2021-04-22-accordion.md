---
layout: post
category: "Web"
tag: "UI Modules"
title: Accordion
subtitle: "A content area which can be collapsed and expanded."
permalink: /web/accordion/
---

## Overview

The accordion component delivers large amounts of content in a small space through progressive disclosure. The header title give the user a high level overview of the content allowing the user to decide which sections to read.<br>

Accordions can make information processing and discovering more effective. However, it does hide content from users and it’s important to account for a user not noticing or reading all of the included content. If a user is likely to read all of the content then don’t use an accordion as it adds the burden of an extra click; instead use a full scrolling page with normal headers.<br>

Accordion is composed of 3 elements: 
Header: contains the section title and is control for revealing the panel.
Icon: indicates if the panel is open or closed.
Panel: the section of content associated with an accordion header.

## When to use
- To organize related information.
- To shorten pages and reduce scrolling when content is not crucial to read in full.
- When space is at a premium and long content cannot be displayed all at once, like on a mobile interface or in a side panel.

### When not to use
- If users need to see most or all of the information on a page. Use well-formatted text instead.
- If there is not enough content to warrant condensing. Accordions increase cognitive load and interaction cost, as users have to make decisions about what headers to click on.

## Guidelines
**Make the entire header selectable.** <br>
Allow users to click anywhere in the header area to expand or collapse the content; a larger target is easier to manipulate.
**Give interactive elements enough space.** <br>
Make sure interactive elements within the collapsible region are far enough from the headers that users don’t accidentally trigger a collapse. (The exact distance depends on the device.)
**Differ content visually.**<br>
The content in the accordion body should be visually different from the rest of the page as it is secondary information. The accordion body is always displayed below its header. Use spacing  and/or hierarchy to structure the body content. 

### Example usage
![Coins Construction Cloud - Design System - UI Module - Accordion]({{site.baseurl}}/img/Example_Usage_Accordion.png)

### Live preview
Include code snippet here
