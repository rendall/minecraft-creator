---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.BlockVolume Interface
description: Contents of the @minecraft/server.BlockVolume class.
---
# BlockVolume Interface

> [!CAUTION]
> This interface is still in pre-release.  Its signature may change or it may be removed in future releases.

A BlockVolume is a simple interface to an object which represents a 3D rectangle of a given size (in blocks) at a world block location.

Note that these are not analogous to "min" and "max" values, in that the vector components are not guaranteed to be in any order.

In addition, these vector positions are not interchangeable with BlockLocation.

If you want to get this volume represented as range of of BlockLocations, you can use the getBoundingBox utility function.

This volume class will maintain the ordering of the corner indexes as initially set. imagine that each corner is assigned in Editor - as you move the corner around (potentially inverting the min/max relationship of the bounds) - what

you had originally selected as the top/left corner would traditionally become the bottom/right.  

When manually editing these kinds of volumes, you need to maintain the identity of the corner as you edit - the BlockVolume utility functions do this.



Important to note that this measures block sizes (to/from) - a normal AABB (0,0,0) to (0,0,0) would traditionally be of size (0,0,0)

However, because we're measuring blocks - the size or span of a BlockVolume would actually be (1,1,1)



## Properties

### **from**
`from: Vector3;`

A world block location that represents a corner in a 3D rectangle

Type: [*Vector3*](Vector3.md)

### **to**
`to: Vector3;`

A world block location that represents the opposite corner in a 3D rectangle

Type: [*Vector3*](Vector3.md)
