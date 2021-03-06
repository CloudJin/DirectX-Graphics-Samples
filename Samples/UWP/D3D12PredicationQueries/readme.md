---
page_type: sample
languages:
- cpp
products:
- windows
- windows-uwp
name: Direct3D 12 predication and queries sample
urlFragment: d3d12-predication-and-queries-sample-uwp
description: This sample demonstrates the use of binary occlusion queries and predication in Direct3D 12.
extendedZipContent:
- path: LICENSE
  target: LICENSE
---

# Direct3D 12 predication and queries sample
![PredicationQueries GUI](src/D3D12PredicationQueries.png)

This sample demonstrates the use of binary occlusion queries and predication in Direct3D 12. The sample renders two quads; one of them animates and periodically occludes the other. For each rendered frame, a binary occlusion query is executed and the SetPredication API is used to conditionally draw the potentially occluded quad. A transparency effect is used to illustrate when the query determines that the quad is fully occluded.

### Optional features
This sample has been updated to build against the Windows 10 Anniversary Update SDK. In this SDK a new revision of Root Signatures is available for Direct3D 12 apps to use. Root Signature 1.1 allows for apps to declare when descriptors in a descriptor heap won't change or the data descriptors point to won't change.  This allows the option for drivers to make optimizations that might be possible knowing that something (like a descriptor or the memory it points to) is static for some period of time.