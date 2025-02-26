---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.DefinitionModifier Class
description: Contents of the @minecraft/server.DefinitionModifier class.
---
# DefinitionModifier Class

> [!CAUTION]
> This class is still in pre-release.  Its signature may change or it may be removed in future releases.

Contains a set of updates to the component definition state of an entity.

## Methods
- [constructor](#constructor)
- [getComponentGroupsToAdd](#getcomponentgroupstoadd)
- [getComponentGroupsToRemove](#getcomponentgroupstoremove)
- [getTriggers](#gettriggers)
- [setComponentGroupsToAdd](#setcomponentgroupstoadd)
- [setComponentGroupsToRemove](#setcomponentgroupstoremove)
- [setTriggers](#settriggers)

### **constructor**
`
new DefinitionModifier()
`

Constructor for a new DefinitionModifier.

#### **Returns** [*DefinitionModifier*](DefinitionModifier.md)

### **getComponentGroupsToAdd**
`
getComponentGroupsToAdd(): string[]
`

Retrieves the list of component groups that will be added via this definition modification.

#### **Returns** *string*[]

### **getComponentGroupsToRemove**
`
getComponentGroupsToRemove(): string[]
`

Retrieves the list of component groups that will be removed via this definition modification.

#### **Returns** *string*[]

### **getTriggers**
`
getTriggers(): Trigger[]
`

Retrieves the list of entity definition events that will be fired via this update.

#### **Returns** [*Trigger*](Trigger.md)[]

### **setComponentGroupsToAdd**
`
setComponentGroupsToAdd(newGroups: string[]): void
`

Updates the list of component groups that will be added via this definition modification.

#### **Parameters**
- **newGroups**: *string*[]

### **setComponentGroupsToRemove**
`
setComponentGroupsToRemove(removedGroups: string[]): void
`

Updates the list of component groups that will be removed via this definition modification.

#### **Parameters**
- **removedGroups**: *string*[]

### **setTriggers**
`
setTriggers(newTriggers: Trigger[]): void
`

Updates the list of entity definition events that will be fired via this update.

#### **Parameters**
- **newTriggers**: [*Trigger*](Trigger.md)[]
