---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server Module
description: Contents of the @minecraft/server module
---
# `@minecraft/server` Module

Contains many types related to manipulating a Minecraft world, including entities, blocks, dimensions, and more.

## [Changelog](changelog.md)

## Manifest Details
```json
{
    "module_name": "@minecraft/server",
    "version": "1.7.0"
}
```

## Available Versions
- `1.8.0-beta`
- `1.7.0`
- `1.6.0`
- `1.5.0`
- `1.4.0`
- `1.3.0`
- `1.2.0`
- `1.1.0`
- `0.1.0`

## Enumerations
- [BlockComponentTypes](BlockComponentTypes.md)
- [BlockVolumeIntersection](BlockVolumeIntersection.md)
- [CompoundBlockVolumeAction](CompoundBlockVolumeAction.md)
- [CompoundBlockVolumePositionRelativity](CompoundBlockVolumePositionRelativity.md)
- [Difficulty](Difficulty.md)
- [Direction](Direction.md)
- [DisplaySlotId](DisplaySlotId.md)
- [DyeColor](DyeColor.md)
- [EasingType](EasingType.md)
- [EntityComponentTypes](EntityComponentTypes.md)
- [EntityDamageCause](EntityDamageCause.md)
- [EntityInitializationCause](EntityInitializationCause.md)
- [EntityLifetimeState](EntityLifetimeState.md)
- [EquipmentSlot](EquipmentSlot.md)
- [FluidType](FluidType.md)
- [GameMode](GameMode.md)
- [ItemComponentTypes](ItemComponentTypes.md)
- [ItemLockMode](ItemLockMode.md)
- [MoonPhase](MoonPhase.md)
- [ObjectiveSortOrder](ObjectiveSortOrder.md)
- [ScoreboardIdentityType](ScoreboardIdentityType.md)
- [ScriptEventSource](ScriptEventSource.md)
- [SignSide](SignSide.md)
- [TimeOfDay](TimeOfDay.md)
- [WatchdogTerminateReason](WatchdogTerminateReason.md)
- [WeatherType](WeatherType.md)

# Type Aliases
- [BlockComponentTypeMap](BlockComponentTypeMap.md)
- [EntityComponentTypeMap](EntityComponentTypeMap.md)
- [ItemComponentTypeMap](ItemComponentTypeMap.md)

## Classes
- [Block](Block.md)
- [BlockAreaSize](BlockAreaSize.md)
- [BlockComponent](BlockComponent.md)
- [BlockEvent](BlockEvent.md)
- [BlockExplodeAfterEvent](BlockExplodeAfterEvent.md)
- [BlockExplodeAfterEventSignal](BlockExplodeAfterEventSignal.md)
- [BlockInventoryComponent](BlockInventoryComponent.md)
- [BlockLavaContainerComponent](BlockLavaContainerComponent.md)
- [BlockLiquidContainerComponent](BlockLiquidContainerComponent.md)
- [BlockLocationIterator](BlockLocationIterator.md)
- [BlockPermutation](BlockPermutation.md)
- [BlockPistonComponent](BlockPistonComponent.md)
- [BlockPotionContainerComponent](BlockPotionContainerComponent.md)
- [BlockRecordPlayerComponent](BlockRecordPlayerComponent.md)
- [BlockSignComponent](BlockSignComponent.md)
- [BlockSnowContainerComponent](BlockSnowContainerComponent.md)
- [BlockStates](BlockStates.md)
- [BlockStateType](BlockStateType.md)
- [BlockType](BlockType.md)
- [BlockTypes](BlockTypes.md)
- [BlockVolumeUtils](BlockVolumeUtils.md)
- [BlockWaterContainerComponent](BlockWaterContainerComponent.md)
- [BoundingBoxUtils](BoundingBoxUtils.md)
- [ButtonPushAfterEvent](ButtonPushAfterEvent.md)
- [ButtonPushAfterEventSignal](ButtonPushAfterEventSignal.md)
- [Camera](Camera.md)
- [ChatSendAfterEvent](ChatSendAfterEvent.md)
- [ChatSendAfterEventSignal](ChatSendAfterEventSignal.md)
- [ChatSendBeforeEvent](ChatSendBeforeEvent.md)
- [ChatSendBeforeEventSignal](ChatSendBeforeEventSignal.md)
- [CommandResult](CommandResult.md)
- [Component](Component.md)
- [CompoundBlockVolume](CompoundBlockVolume.md)
- [Container](Container.md)
- [ContainerSlot](ContainerSlot.md)
- [DataDrivenEntityTriggerAfterEvent](DataDrivenEntityTriggerAfterEvent.md)
- [DataDrivenEntityTriggerAfterEventSignal](DataDrivenEntityTriggerAfterEventSignal.md)
- [DataDrivenEntityTriggerBeforeEvent](DataDrivenEntityTriggerBeforeEvent.md)
- [DataDrivenEntityTriggerBeforeEventSignal](DataDrivenEntityTriggerBeforeEventSignal.md)
- [DefinitionModifier](DefinitionModifier.md)
- [Dimension](Dimension.md)
- [DimensionType](DimensionType.md)
- [DimensionTypes](DimensionTypes.md)
- [Effect](Effect.md)
- [EffectAddAfterEvent](EffectAddAfterEvent.md)
- [EffectAddAfterEventSignal](EffectAddAfterEventSignal.md)
- [EffectAddBeforeEvent](EffectAddBeforeEvent.md)
- [EffectAddBeforeEventSignal](EffectAddBeforeEventSignal.md)
- [EffectType](EffectType.md)
- [EffectTypes](EffectTypes.md)
- [Enchantment](Enchantment.md)
- [EnchantmentList](EnchantmentList.md)
- [EnchantmentSlot](EnchantmentSlot.md)
- [EnchantmentType](EnchantmentType.md)
- [EnchantmentTypes](EnchantmentTypes.md)
- [Entity](Entity.md)
- [EntityAddRiderComponent](EntityAddRiderComponent.md)
- [EntityAgeableComponent](EntityAgeableComponent.md)
- [EntityAttributeComponent](EntityAttributeComponent.md)
- [EntityBaseMovementComponent](EntityBaseMovementComponent.md)
- [EntityBreathableComponent](EntityBreathableComponent.md)
- [EntityCanClimbComponent](EntityCanClimbComponent.md)
- [EntityCanFlyComponent](EntityCanFlyComponent.md)
- [EntityCanPowerJumpComponent](EntityCanPowerJumpComponent.md)
- [EntityColorComponent](EntityColorComponent.md)
- [EntityComponent](EntityComponent.md)
- [EntityDefinitionFeedItem](EntityDefinitionFeedItem.md)
- [EntityDieAfterEvent](EntityDieAfterEvent.md)
- [EntityDieAfterEventSignal](EntityDieAfterEventSignal.md)
- [EntityEquippableComponent](EntityEquippableComponent.md)
- [EntityFireImmuneComponent](EntityFireImmuneComponent.md)
- [EntityFloatsInLiquidComponent](EntityFloatsInLiquidComponent.md)
- [EntityFlyingSpeedComponent](EntityFlyingSpeedComponent.md)
- [EntityFrictionModifierComponent](EntityFrictionModifierComponent.md)
- [EntityGroundOffsetComponent](EntityGroundOffsetComponent.md)
- [EntityHealableComponent](EntityHealableComponent.md)
- [EntityHealthChangedAfterEvent](EntityHealthChangedAfterEvent.md)
- [EntityHealthChangedAfterEventSignal](EntityHealthChangedAfterEventSignal.md)
- [EntityHealthComponent](EntityHealthComponent.md)
- [EntityHitBlockAfterEvent](EntityHitBlockAfterEvent.md)
- [EntityHitBlockAfterEventSignal](EntityHitBlockAfterEventSignal.md)
- [EntityHitEntityAfterEvent](EntityHitEntityAfterEvent.md)
- [EntityHitEntityAfterEventSignal](EntityHitEntityAfterEventSignal.md)
- [EntityHurtAfterEvent](EntityHurtAfterEvent.md)
- [EntityHurtAfterEventSignal](EntityHurtAfterEventSignal.md)
- [EntityInventoryComponent](EntityInventoryComponent.md)
- [EntityIsBabyComponent](EntityIsBabyComponent.md)
- [EntityIsChargedComponent](EntityIsChargedComponent.md)
- [EntityIsChestedComponent](EntityIsChestedComponent.md)
- [EntityIsDyeableComponent](EntityIsDyeableComponent.md)
- [EntityIsHiddenWhenInvisibleComponent](EntityIsHiddenWhenInvisibleComponent.md)
- [EntityIsIgnitedComponent](EntityIsIgnitedComponent.md)
- [EntityIsIllagerCaptainComponent](EntityIsIllagerCaptainComponent.md)
- [EntityIsSaddledComponent](EntityIsSaddledComponent.md)
- [EntityIsShakingComponent](EntityIsShakingComponent.md)
- [EntityIsShearedComponent](EntityIsShearedComponent.md)
- [EntityIsStackableComponent](EntityIsStackableComponent.md)
- [EntityIsStunnedComponent](EntityIsStunnedComponent.md)
- [EntityIsTamedComponent](EntityIsTamedComponent.md)
- [EntityItemComponent](EntityItemComponent.md)
- [EntityIterator](EntityIterator.md)
- [EntityLavaMovementComponent](EntityLavaMovementComponent.md)
- [EntityLeashableComponent](EntityLeashableComponent.md)
- [EntityLoadAfterEvent](EntityLoadAfterEvent.md)
- [EntityLoadAfterEventSignal](EntityLoadAfterEventSignal.md)
- [EntityMarkVariantComponent](EntityMarkVariantComponent.md)
- [EntityMountTamingComponent](EntityMountTamingComponent.md)
- [EntityMovementAmphibiousComponent](EntityMovementAmphibiousComponent.md)
- [EntityMovementBasicComponent](EntityMovementBasicComponent.md)
- [EntityMovementComponent](EntityMovementComponent.md)
- [EntityMovementFlyComponent](EntityMovementFlyComponent.md)
- [EntityMovementGenericComponent](EntityMovementGenericComponent.md)
- [EntityMovementGlideComponent](EntityMovementGlideComponent.md)
- [EntityMovementHoverComponent](EntityMovementHoverComponent.md)
- [EntityMovementJumpComponent](EntityMovementJumpComponent.md)
- [EntityMovementSkipComponent](EntityMovementSkipComponent.md)
- [EntityMovementSwayComponent](EntityMovementSwayComponent.md)
- [EntityNavigationClimbComponent](EntityNavigationClimbComponent.md)
- [EntityNavigationComponent](EntityNavigationComponent.md)
- [EntityNavigationFloatComponent](EntityNavigationFloatComponent.md)
- [EntityNavigationFlyComponent](EntityNavigationFlyComponent.md)
- [EntityNavigationGenericComponent](EntityNavigationGenericComponent.md)
- [EntityNavigationHoverComponent](EntityNavigationHoverComponent.md)
- [EntityNavigationWalkComponent](EntityNavigationWalkComponent.md)
- [EntityOnFireComponent](EntityOnFireComponent.md)
- [EntityPushThroughComponent](EntityPushThroughComponent.md)
- [EntityRemoveAfterEvent](EntityRemoveAfterEvent.md)
- [EntityRemoveAfterEventSignal](EntityRemoveAfterEventSignal.md)
- [EntityRemoveBeforeEvent](EntityRemoveBeforeEvent.md)
- [EntityRemoveBeforeEventSignal](EntityRemoveBeforeEventSignal.md)
- [EntityRideableComponent](EntityRideableComponent.md)
- [EntityRidingComponent](EntityRidingComponent.md)
- [EntityScaleComponent](EntityScaleComponent.md)
- [EntitySkinIdComponent](EntitySkinIdComponent.md)
- [EntitySpawnAfterEvent](EntitySpawnAfterEvent.md)
- [EntitySpawnAfterEventSignal](EntitySpawnAfterEventSignal.md)
- [EntityStrengthComponent](EntityStrengthComponent.md)
- [EntityTameableComponent](EntityTameableComponent.md)
- [EntityType](EntityType.md)
- [EntityTypeIterator](EntityTypeIterator.md)
- [EntityTypes](EntityTypes.md)
- [EntityUnderwaterMovementComponent](EntityUnderwaterMovementComponent.md)
- [EntityVariantComponent](EntityVariantComponent.md)
- [EntityWantsJockeyComponent](EntityWantsJockeyComponent.md)
- [ExplosionAfterEvent](ExplosionAfterEvent.md)
- [ExplosionAfterEventSignal](ExplosionAfterEventSignal.md)
- [ExplosionBeforeEvent](ExplosionBeforeEvent.md)
- [ExplosionBeforeEventSignal](ExplosionBeforeEventSignal.md)
- [FeedItem](FeedItem.md)
- [FeedItemEffect](FeedItemEffect.md)
- [FilterGroup](FilterGroup.md)
- [FluidContainer](FluidContainer.md)
- [IButtonPushAfterEventSignal](IButtonPushAfterEventSignal.md)
- [ILeverActionAfterEventSignal](ILeverActionAfterEventSignal.md)
- [IPlayerJoinAfterEventSignal](IPlayerJoinAfterEventSignal.md)
- [IPlayerLeaveAfterEventSignal](IPlayerLeaveAfterEventSignal.md)
- [IPlayerSpawnAfterEventSignal](IPlayerSpawnAfterEventSignal.md)
- [ItemCompleteUseAfterEvent](ItemCompleteUseAfterEvent.md)
- [ItemCompleteUseAfterEventSignal](ItemCompleteUseAfterEventSignal.md)
- [ItemComponent](ItemComponent.md)
- [ItemCooldownComponent](ItemCooldownComponent.md)
- [ItemDefinitionAfterEventSignal](ItemDefinitionAfterEventSignal.md)
- [ItemDefinitionBeforeEventSignal](ItemDefinitionBeforeEventSignal.md)
- [ItemDefinitionTriggeredAfterEvent](ItemDefinitionTriggeredAfterEvent.md)
- [ItemDefinitionTriggeredBeforeEvent](ItemDefinitionTriggeredBeforeEvent.md)
- [ItemDurabilityComponent](ItemDurabilityComponent.md)
- [ItemEnchantsComponent](ItemEnchantsComponent.md)
- [ItemFoodComponent](ItemFoodComponent.md)
- [ItemReleaseUseAfterEvent](ItemReleaseUseAfterEvent.md)
- [ItemReleaseUseAfterEventSignal](ItemReleaseUseAfterEventSignal.md)
- [ItemStack](ItemStack.md)
- [ItemStartUseAfterEvent](ItemStartUseAfterEvent.md)
- [ItemStartUseAfterEventSignal](ItemStartUseAfterEventSignal.md)
- [ItemStartUseOnAfterEvent](ItemStartUseOnAfterEvent.md)
- [ItemStartUseOnAfterEventSignal](ItemStartUseOnAfterEventSignal.md)
- [ItemStopUseAfterEvent](ItemStopUseAfterEvent.md)
- [ItemStopUseAfterEventSignal](ItemStopUseAfterEventSignal.md)
- [ItemStopUseOnAfterEvent](ItemStopUseOnAfterEvent.md)
- [ItemStopUseOnAfterEventSignal](ItemStopUseOnAfterEventSignal.md)
- [ItemType](ItemType.md)
- [ItemTypes](ItemTypes.md)
- [ItemUseAfterEvent](ItemUseAfterEvent.md)
- [ItemUseAfterEventSignal](ItemUseAfterEventSignal.md)
- [ItemUseBeforeEvent](ItemUseBeforeEvent.md)
- [ItemUseBeforeEventSignal](ItemUseBeforeEventSignal.md)
- [ItemUseOnAfterEvent](ItemUseOnAfterEvent.md)
- [ItemUseOnAfterEventSignal](ItemUseOnAfterEventSignal.md)
- [ItemUseOnBeforeEvent](ItemUseOnBeforeEvent.md)
- [ItemUseOnBeforeEventSignal](ItemUseOnBeforeEventSignal.md)
- [LeverActionAfterEvent](LeverActionAfterEvent.md)
- [LeverActionAfterEventSignal](LeverActionAfterEventSignal.md)
- [MessageReceiveAfterEvent](MessageReceiveAfterEvent.md)
- [MinecraftDimensionTypes](MinecraftDimensionTypes.md)
- [MolangVariableMap](MolangVariableMap.md)
- [NavigationResult](NavigationResult.md)
- [PistonActivateAfterEvent](PistonActivateAfterEvent.md)
- [PistonActivateAfterEventSignal](PistonActivateAfterEventSignal.md)
- [PistonActivateBeforeEvent](PistonActivateBeforeEvent.md)
- [PistonActivateBeforeEventSignal](PistonActivateBeforeEventSignal.md)
- [Player](Player.md)
- [PlayerBreakBlockAfterEvent](PlayerBreakBlockAfterEvent.md)
- [PlayerBreakBlockAfterEventSignal](PlayerBreakBlockAfterEventSignal.md)
- [PlayerBreakBlockBeforeEvent](PlayerBreakBlockBeforeEvent.md)
- [PlayerBreakBlockBeforeEventSignal](PlayerBreakBlockBeforeEventSignal.md)
- [PlayerDimensionChangeAfterEvent](PlayerDimensionChangeAfterEvent.md)
- [PlayerDimensionChangeAfterEventSignal](PlayerDimensionChangeAfterEventSignal.md)
- [PlayerInteractWithBlockAfterEvent](PlayerInteractWithBlockAfterEvent.md)
- [PlayerInteractWithBlockAfterEventSignal](PlayerInteractWithBlockAfterEventSignal.md)
- [PlayerInteractWithBlockBeforeEvent](PlayerInteractWithBlockBeforeEvent.md)
- [PlayerInteractWithBlockBeforeEventSignal](PlayerInteractWithBlockBeforeEventSignal.md)
- [PlayerInteractWithEntityAfterEvent](PlayerInteractWithEntityAfterEvent.md)
- [PlayerInteractWithEntityAfterEventSignal](PlayerInteractWithEntityAfterEventSignal.md)
- [PlayerInteractWithEntityBeforeEvent](PlayerInteractWithEntityBeforeEvent.md)
- [PlayerInteractWithEntityBeforeEventSignal](PlayerInteractWithEntityBeforeEventSignal.md)
- [PlayerIterator](PlayerIterator.md)
- [PlayerJoinAfterEvent](PlayerJoinAfterEvent.md)
- [PlayerJoinAfterEventSignal](PlayerJoinAfterEventSignal.md)
- [PlayerLeaveAfterEvent](PlayerLeaveAfterEvent.md)
- [PlayerLeaveAfterEventSignal](PlayerLeaveAfterEventSignal.md)
- [PlayerLeaveBeforeEvent](PlayerLeaveBeforeEvent.md)
- [PlayerLeaveBeforeEventSignal](PlayerLeaveBeforeEventSignal.md)
- [PlayerPlaceBlockAfterEvent](PlayerPlaceBlockAfterEvent.md)
- [PlayerPlaceBlockAfterEventSignal](PlayerPlaceBlockAfterEventSignal.md)
- [PlayerPlaceBlockBeforeEvent](PlayerPlaceBlockBeforeEvent.md)
- [PlayerPlaceBlockBeforeEventSignal](PlayerPlaceBlockBeforeEventSignal.md)
- [PlayerSpawnAfterEvent](PlayerSpawnAfterEvent.md)
- [PlayerSpawnAfterEventSignal](PlayerSpawnAfterEventSignal.md)
- [PressurePlatePopAfterEvent](PressurePlatePopAfterEvent.md)
- [PressurePlatePopAfterEventSignal](PressurePlatePopAfterEventSignal.md)
- [PressurePlatePushAfterEvent](PressurePlatePushAfterEvent.md)
- [PressurePlatePushAfterEventSignal](PressurePlatePushAfterEventSignal.md)
- [ProjectileHitBlockAfterEvent](ProjectileHitBlockAfterEvent.md)
- [ProjectileHitBlockAfterEventSignal](ProjectileHitBlockAfterEventSignal.md)
- [ProjectileHitEntityAfterEvent](ProjectileHitEntityAfterEvent.md)
- [ProjectileHitEntityAfterEventSignal](ProjectileHitEntityAfterEventSignal.md)
- [Scoreboard](Scoreboard.md)
- [ScoreboardIdentity](ScoreboardIdentity.md)
- [ScoreboardObjective](ScoreboardObjective.md)
- [ScoreboardScoreInfo](ScoreboardScoreInfo.md)
- [ScreenDisplay](ScreenDisplay.md)
- [ScriptEventCommandMessageAfterEvent](ScriptEventCommandMessageAfterEvent.md)
- [ScriptEventCommandMessageAfterEventSignal](ScriptEventCommandMessageAfterEventSignal.md)
- [Seat](Seat.md)
- [ServerMessageAfterEventSignal](ServerMessageAfterEventSignal.md)
- [System](System.md)
- [SystemAfterEvents](SystemAfterEvents.md)
- [SystemBeforeEvents](SystemBeforeEvents.md)
- [TargetBlockHitAfterEvent](TargetBlockHitAfterEvent.md)
- [TargetBlockHitAfterEventSignal](TargetBlockHitAfterEventSignal.md)
- [Trigger](Trigger.md)
- [TripWireTripAfterEvent](TripWireTripAfterEvent.md)
- [TripWireTripAfterEventSignal](TripWireTripAfterEventSignal.md)
- [Vector](Vector.md)
- [WatchdogTerminateBeforeEvent](WatchdogTerminateBeforeEvent.md)
- [WatchdogTerminateBeforeEventSignal](WatchdogTerminateBeforeEventSignal.md)
- [WeatherChangeAfterEvent](WeatherChangeAfterEvent.md)
- [WeatherChangeAfterEventSignal](WeatherChangeAfterEventSignal.md)
- [World](World.md)
- [WorldAfterEvents](WorldAfterEvents.md)
- [WorldBeforeEvents](WorldBeforeEvents.md)
- [WorldInitializeAfterEvent](WorldInitializeAfterEvent.md)
- [WorldInitializeAfterEventSignal](WorldInitializeAfterEventSignal.md)

## Interfaces
- [BlockEventOptions](BlockEventOptions.md)
- [BlockFillOptions](BlockFillOptions.md)
- [BlockHitInformation](BlockHitInformation.md)
- [BlockRaycastHit](BlockRaycastHit.md)
- [BlockRaycastOptions](BlockRaycastOptions.md)
- [BlockVolume](BlockVolume.md)
- [BoundingBox](BoundingBox.md)
- [CameraDefaultOptions](CameraDefaultOptions.md)
- [CameraEaseOptions](CameraEaseOptions.md)
- [CameraFadeOptions](CameraFadeOptions.md)
- [CameraFadeTimeOptions](CameraFadeTimeOptions.md)
- [CameraSetFacingOptions](CameraSetFacingOptions.md)
- [CameraSetLocationOptions](CameraSetLocationOptions.md)
- [CameraSetPosOptions](CameraSetPosOptions.md)
- [CameraSetRotOptions](CameraSetRotOptions.md)
- [CompoundBlockVolumeItem](CompoundBlockVolumeItem.md)
- [DimensionLocation](DimensionLocation.md)
- [EntityApplyDamageByProjectileOptions](EntityApplyDamageByProjectileOptions.md)
- [EntityApplyDamageOptions](EntityApplyDamageOptions.md)
- [EntityDamageSource](EntityDamageSource.md)
- [EntityDataDrivenTriggerEventOptions](EntityDataDrivenTriggerEventOptions.md)
- [EntityEffectOptions](EntityEffectOptions.md)
- [EntityEventOptions](EntityEventOptions.md)
- [EntityHitInformation](EntityHitInformation.md)
- [EntityQueryOptions](EntityQueryOptions.md)
- [EntityQueryScoreOptions](EntityQueryScoreOptions.md)
- [EntityRaycastHit](EntityRaycastHit.md)
- [EntityRaycastOptions](EntityRaycastOptions.md)
- [ExplosionOptions](ExplosionOptions.md)
- [MusicOptions](MusicOptions.md)
- [NumberRange](NumberRange.md)
- [PlayAnimationOptions](PlayAnimationOptions.md)
- [PlayerSoundOptions](PlayerSoundOptions.md)
- [RawMessage](RawMessage.md)
- [RawMessageScore](RawMessageScore.md)
- [RawText](RawText.md)
- [RGB](RGB.md)
- [RGBA](RGBA.md)
- [ScoreboardObjectiveDisplayOptions](ScoreboardObjectiveDisplayOptions.md)
- [ScriptEventMessageFilterOptions](ScriptEventMessageFilterOptions.md)
- [TeleportOptions](TeleportOptions.md)
- [TitleDisplayOptions](TitleDisplayOptions.md)
- [Vector2](Vector2.md)
- [Vector3](Vector3.md)
- [WorldSoundOptions](WorldSoundOptions.md)

## Errors
- [CommandError](CommandError.md)
- [LocationInUnloadedChunkError](LocationInUnloadedChunkError.md)
- [LocationOutOfWorldBoundariesError](LocationOutOfWorldBoundariesError.md)

## Constants

### **MoonPhaseCount**
`static read-only MoonPhaseCount = 8;`

Holds the number of MoonPhases

Type: *number*

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

### **TicksPerDay**
`static read-only TicksPerDay = 24000;`

Type: *number*

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

### **TicksPerSecond**
`static read-only TicksPerSecond = 20;`

How many times the server ticks per second of real time.

Type: *number*

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

## Objects
  
### **system**
`static read-only system: System;`

A class that provides system-level events and functions.

Type: [*System*](System.md)
  
### **world**
`static read-only world: World;`

A class that wraps the state of a world - a set of dimensions and the environment of Minecraft.

Type: [*World*](World.md)
