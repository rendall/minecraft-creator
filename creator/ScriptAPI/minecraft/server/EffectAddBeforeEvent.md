---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.EffectAddBeforeEvent Class
description: Contents of the @minecraft/server.EffectAddBeforeEvent class.
---
# EffectAddBeforeEvent Class

> [!CAUTION]
> This class is still in pre-release.  Its signature may change or it may be removed in future releases.

Contains information related to changes to an effect - like poison - being added to an entity.

## Properties

### **cancel**
`cancel: boolean;`

When set to true will cancel the event.

Type: *boolean*

### **duration**
`duration: number;`

Effect duration.

Type: *number*

### **effectType**
`read-only effectType: string;`

The type of the effect that is being added.

Type: *string*

### **entity**
`read-only entity: Entity;`

Entity that the effect is being added to.

Type: [*Entity*](Entity.md)
