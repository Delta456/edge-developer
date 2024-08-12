---
title: Overview and timelines for migrating to Manifest V3
description: Timelines for migration from Manifest V2 to V3, and overview of V3, which reduces fragmentation of the web for developers and enhances privacy, security, and performance for end users.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: conceptual
ms.service: microsoft-edge
ms.subservice: extensions
ms.date: 08/12/2024
---
# Overview and timelines for migrating to Manifest V3

A _manifest file_ is the blueprint of an extension.  A manifest file for an extension includes information such as the version number of the extension, the title of the extension, and permissions needed to run the extension.  The manifest file follows the format specified by Manifest V2 or Manifest V3.


<!-- ====================================================================== -->
## Overview of changes in Manifest V3

Migrating from Manifest V2 to Manifest V3 brings several structural changes to how extensions are handled by the browser.

In October 2020, Microsoft announced the [decision to embrace Manifest V3](https://blogs.windows.com/msedgedev/2020/10/14/extension-manifest-chromium-edge/) to help reduce fragmentation of the web for all developers and enhance privacy, security, and performance for end users.

Manifest V3 is an initiative of the [Chromium project](https://www.chromium.org/Home/).

An overview of the changes involved, as described in [Migrate to Manifest V3](https://developer.chrome.com/docs/extensions/develop/migrate):

* Background pages have been replaced by service workers.

* Network request modifications are now handled by the new `declarativeNetRequest` API.

* Remotely hosted code is no longer allowed.  An extension can only run JavaScript that's included within its own package.

* Support for Promises has been added to many methods.  Callbacks are still supported, as an alternative.

* Various minor feature improvements.


<!-- ====================================================================== -->
## Manifest timeline for the Chromium browser engine

Chromium has revised the timelines for ending support for Manifest V2.  See:

* [Manifest V2 support timeline](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline)
* [The phase-out timeline](https://developer.chrome.com/blog/resuming-the-transition-to-mv3#the_phase-out_timeline) in _Resuming the transition to Manifest V3_.


<!-- ====================================================================== -->
## Manifest timeline for Microsoft Edge and Partner Center

To help you plan the migration of your extension from Manifest V2 to Manifest V3, consider the following schedule for support for Manifest V2 and V3 in Microsoft Edge and Microsoft Partner Center.

The Microsoft Edge team will independently decide on MV3 migration timelines for Microsoft Edge Add-ons and share an update here.  We continue to analyze the concerns raised by extension developers and explore the optimal path for the Microsoft Edge Add-ons ecosystem.  Meanwhile, to plan the migration of your extension from Manifest V2 to Manifest V3, see [Manifest timeline for the Chromium browser engine](#manifest-timeline-for-the-chromium-browser-engine), above.


**The Microsoft Edge team is currently in the process of updating this MV3 migration timeline.**

| Timeframe | Microsoft Partner Center changes | Microsoft Edge changes |
|--- |--- |--- |
| July 2022 (already in effect) | Microsoft Partner Center will no longer accept new Manifest V2 extensions with visibility set as `Hidden` or `Public`. | No change. |
| TBD | Microsoft Partner Center will no longer accept updates to existing Manifest V2 extensions. Developers can submit updates for migrating a V2 extension to V3. | Microsoft Edge stops running Manifest V2 extensions. Enterprises can allow Manifest V2 extensions to run on Microsoft Edge, by using enterprise policies. |
| TBD | No change. | Manifest V2 extensions will no longer function in Microsoft Edge, even with the use of enterprise policies. |


<!-- ------------------------------ -->
#### Timeline for MV2-based extensions

The move to Manifest V3 improves the security, privacy, and performance of extensions.  Our current strategy for Microsoft Edge is to support new MV3-based extensions and support updates to existing MV2-based extensions from our partner ecosystem.  Microsoft Edge Extensions will continue to support updates for MV2-based extensions for an extended period of time, and we will communicate with our partner ecosystem when we plan the deprecation of existing MV2-based extensions.  For enterprises, Manifest V2 extensions will continue to be supported through Enterprise policies at least until the date in the Chromium Manifest V2 support timeline.


<!-- ====================================================================== -->
## Providing feedback

Microsoft continues to iteratively improve the platform and address the feedback shared by extension developers.  Share your questions, comments, and concerns with the team on Twitter [@MSEdgeDev](https://twitter.com/msedgedev/) or via the [Microsoft Edge Insider forums on TechCommunity](https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254).

See also:
* [Participate in the discussion forum](https://learn.microsoft.com/en-us/microsoft-edge/extensions-chromium/publish/contact-extensions-team#participate-in-the-discussion-forum) in _Contact Microsoft Edge extensions support_.


<!-- ---------------------------------------------------------------------- -->
## See also

* [Migrate to Manifest V3](https://developer.chrome.com/docs/extensions/develop/migrate)
* [Manifest V2 support timeline](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline)
* [The phase-out timeline](https://developer.chrome.com/blog/resuming-the-transition-to-mv3#the_phase-out_timeline) in _Resuming the transition to Manifest V3_.
