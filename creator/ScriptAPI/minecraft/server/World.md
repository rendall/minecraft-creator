---
# DO NOT TOUCH — This file was automatically generated. See https://github.com/mojang/minecraftapidocsgenerator to modify descriptions, examples, etc.
author: jakeshirley
ms.author: jashir
ms.service: minecraft-bedrock-edition
title: minecraft/server.World Class
description: Contents of the @minecraft/server.World class.
---
# World Class

A class that wraps the state of a world - a set of dimensions and the environment of Minecraft.

## Properties

### **afterEvents**
`read-only afterEvents: WorldAfterEvents;`

Contains a set of events that are applicable to the entirety of the world.  Event callbacks are called in a deferred manner. Event callbacks are executed in read-write mode.

Type: [*WorldAfterEvents*](WorldAfterEvents.md)

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

### **beforeEvents**
`read-only beforeEvents: WorldBeforeEvents;`

Contains a set of events that are applicable to the entirety of the world. Event callbacks are called immediately. Event callbacks are executed in read-only mode.

Type: [*WorldBeforeEvents*](WorldBeforeEvents.md)

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

### **scoreboard**
`read-only scoreboard: Scoreboard;`

Returns the general global scoreboard that applies to the world.

Type: [*Scoreboard*](Scoreboard.md)

> [!CAUTION]
> This property is still in pre-release.  Its signature may change or it may be removed in future releases.

## Methods
- [broadcastClientMessage](#broadcastclientmessage)
- [clearDynamicProperties](#cleardynamicproperties)
- [getAbsoluteTime](#getabsolutetime)
- [getAllPlayers](#getallplayers)
- [getDay](#getday)
- [getDefaultSpawnLocation](#getdefaultspawnlocation)
- [getDimension](#getdimension)
- [getDynamicProperty](#getdynamicproperty)
- [getDynamicPropertyIds](#getdynamicpropertyids)
- [getDynamicPropertyTotalByteCount](#getdynamicpropertytotalbytecount)
- [getEntity](#getentity)
- [getMoonPhase](#getmoonphase)
- [getPlayers](#getplayers)
- [getTimeOfDay](#gettimeofday)
- [playMusic](#playmusic)
- [playSound](#playsound)
- [queueMusic](#queuemusic)
- [sendMessage](#sendmessage)
- [setAbsoluteTime](#setabsolutetime)
- [setDefaultSpawnLocation](#setdefaultspawnlocation)
- [setDynamicProperty](#setdynamicproperty)
- [setTimeOfDay](#settimeofday)
- [stopMusic](#stopmusic)

### **broadcastClientMessage**
`
broadcastClientMessage(id: string, value: string): void
`

A method that is internal-only, used for broadcasting specific messages between client and server.

#### **Parameters**
- **id**: *string*
  
  The message identifier.
- **value**: *string*
  
  The message.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!IMPORTANT]
> This function can't be called in read-only mode.

### **clearDynamicProperties**
`
clearDynamicProperties(): void
`

Clears the set of dynamic properties declared for this behavior pack within the world.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

### **getAbsoluteTime**
`
getAbsoluteTime(): number
`

Returns the absolute time since the start of the world.

#### **Returns** *number*

### **getAllPlayers**
`
getAllPlayers(): Player[]
`

Returns an array of all active players within the world.

#### **Returns** [*Player*](Player.md)[]

> [!WARNING]
> This function can throw errors.

### **getDay**
`
getDay(): number
`

Returns the current day.

#### **Returns** *number* - The current day, determined by the world time divided by the number of ticks per day. New worlds start at day 0.

### **getDefaultSpawnLocation**
`
getDefaultSpawnLocation(): Vector3
`

Returns the default Overworld spawn location. 

#### **Returns** [*Vector3*](Vector3.md) - The default Overworld spawn location. By default, the Y coordinate is 32767, indicating a player's spawn height is not fixed and will be determined by surrounding blocks.

### **getDimension**
`
getDimension(dimensionId: string): Dimension
`

Returns a dimension object.

#### **Parameters**
- **dimensionId**: *string*
  
  The name of the dimension. For example, "overworld", "nether" or "the_end".

#### **Returns** [*Dimension*](Dimension.md) - The requested dimension

> [!WARNING]
> Throws if the given dimension name is invalid

### **getDynamicProperty**
`
getDynamicProperty(identifier: string): boolean | number | string | Vector3 | undefined
`

Returns a property value.

#### **Parameters**
- **identifier**: *string*
  
  The property identifier.

#### **Returns** *boolean* | *number* | *string* | [*Vector3*](Vector3.md) | *undefined* - Returns the value for the property, or undefined if the property has not been set.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!WARNING]
> Throws if the given dynamic property identifier is not defined.

#### Examples
##### ***incrementProperty.ts***
```typescript
  let number = mc.world.getDynamicProperty("samplelibrary:number");

  log("Current value is: " + number);

  if (number === undefined) {
    number = 0;
  }

  if (typeof number !== "number") {
    log("Number is of an unexpected type.");
    return -1;
  }

  mc.world.setDynamicProperty("samplelibrary:number", number + 1);
```
##### ***incrementPropertyInJsonBlob.ts***
```typescript
  let paintStr = mc.world.getDynamicProperty("samplelibrary:longerjson");
  let paint: { color: string; intensity: number } | undefined = undefined;

  log("Current value is: " + paintStr);

  if (paintStr === undefined) {
    paint = {
      color: "purple",
      intensity: 0,
    };
  } else {
    if (typeof paintStr !== "string") {
      log("Paint is of an unexpected type.");
      return -1;
    }

    try {
      paint = JSON.parse(paintStr);
    } catch (e) {
      log("Error parsing serialized struct.");
      return -1;
    }
  }

  if (!paint) {
    log("Error parsing serialized struct.");
    return -1;
  }

  paint.intensity++;
  paintStr = JSON.stringify(paint); // be very careful to ensure your serialized JSON str cannot exceed limits
  mc.world.setDynamicProperty("samplelibrary:longerjson", paintStr);
```

### **getDynamicPropertyIds**
`
getDynamicPropertyIds(): string[]
`

Gets a set of dynamic property identifiers that have been set in this world.

#### **Returns** *string*[] - A string array of active dynamic property identifiers.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

### **getDynamicPropertyTotalByteCount**
`
getDynamicPropertyTotalByteCount(): number
`

Gets the total byte count of dynamic properties. This could potentially be used for your own analytics to ensure you're not storing gigantic sets of dynamic properties.

#### **Returns** *number*

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

### **getEntity**
`
getEntity(id: string): Entity | undefined
`

Returns an entity based on the provided id.

#### **Parameters**
- **id**: *string*
  
  The id of the entity.

#### **Returns** [*Entity*](Entity.md) | *undefined* - The requested entity object.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!WARNING]
> Throws if the given entity id is invalid.

### **getMoonPhase**
`
getMoonPhase(): MoonPhase
`

Returns the MoonPhase for the current time.

#### **Returns** [*MoonPhase*](MoonPhase.md)

### **getPlayers**
`
getPlayers(options?: EntityQueryOptions): Player[]
`

Returns a set of players based on a set of conditions defined via the EntityQueryOptions set of filter criteria.

#### **Parameters**
- **options**?: [*EntityQueryOptions*](EntityQueryOptions.md) = `null`
  
  Additional options that can be used to filter the set of players returned.

#### **Returns** [*Player*](Player.md)[] - A player array.

> [!WARNING]
> Throws if the provided EntityQueryOptions are invalid.

### **getTimeOfDay**
`
getTimeOfDay(): number
`

Returns the time of day.

#### **Returns** *number* - The time of day, in ticks, between 0 and 24000.

### **playMusic**
`
playMusic(trackId: string, musicOptions?: MusicOptions): void
`

Plays a particular music track for all players.

#### **Parameters**
- **trackId**: *string*
- **musicOptions**?: [*MusicOptions*](MusicOptions.md) = `null`

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> This function can throw errors.

#### Examples
##### ***playMusicAndSound.ts***
```typescript
  let players = mc.world.getPlayers();

  const musicOptions: mc.MusicOptions = {
    fade: 0.5,
    loop: true,
    volume: 1.0,
  };
  mc.world.playMusic("music.menu", musicOptions);

  const worldSoundOptions: mc.WorldSoundOptions = {
    pitch: 0.5,
    volume: 4.0,
  };
  mc.world.playSound("ambient.weather.thunder", targetLocation, worldSoundOptions);

  const playerSoundOptions: mc.PlayerSoundOptions = {
    pitch: 1.0,
    volume: 1.0,
  };

  players[0].playSound("bucket.fill_water", playerSoundOptions);
```

### **playSound**
`
playSound(soundId: string, location: Vector3, soundOptions?: WorldSoundOptions): void
`

Plays a sound for all players.

#### **Parameters**
- **soundId**: *string*
- **location**: [*Vector3*](Vector3.md)
- **soundOptions**?: [*WorldSoundOptions*](WorldSoundOptions.md) = `null`

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,An error will be thrown if pitch is less than 0.01.,An error will be thrown if volume is less than 0.0.

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,An error will be thrown if pitch is less than 0.01.,An error will be thrown if volume is less than 0.0.

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,An error will be thrown if pitch is less than 0.01.,An error will be thrown if volume is less than 0.0.

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,An error will be thrown if pitch is less than 0.01.,An error will be thrown if volume is less than 0.0.

#### Examples
##### ***playMusicAndSound.ts***
```typescript
  let players = mc.world.getPlayers();

  const musicOptions: mc.MusicOptions = {
    fade: 0.5,
    loop: true,
    volume: 1.0,
  };
  mc.world.playMusic("music.menu", musicOptions);

  const worldSoundOptions: mc.WorldSoundOptions = {
    pitch: 0.5,
    volume: 4.0,
  };
  mc.world.playSound("ambient.weather.thunder", targetLocation, worldSoundOptions);

  const playerSoundOptions: mc.PlayerSoundOptions = {
    pitch: 1.0,
    volume: 1.0,
  };

  players[0].playSound("bucket.fill_water", playerSoundOptions);
```

### **queueMusic**
`
queueMusic(trackId: string, musicOptions?: MusicOptions): void
`

Queues an additional music track for players. If a track is not playing, a music track will play.

#### **Parameters**
- **trackId**: *string*
  
  Identifier of the music track to play.
- **musicOptions**?: [*MusicOptions*](MusicOptions.md) = `null`
  
  Additional options for the music track.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,

> [!WARNING]
> An error will be thrown if volume is less than 0.0.,An error will be thrown if fade is less than 0.0.,

### **sendMessage**
`
sendMessage(message: (RawMessage | string)[] | RawMessage | string): void
`

Sends a message to all players.

#### **Parameters**
- **message**: ([*RawMessage*](RawMessage.md) | *string*)[] | [*RawMessage*](RawMessage.md) | *string*
  
  The message to be displayed.

> [!WARNING]
> This method can throw if the provided [*@minecraft/server.RawMessage*](../../minecraft/server/RawMessage.md) is in an invalid format. For example, if an empty `name` string is provided to `score`.

#### Examples
##### ***nestedTranslation.ts***
```typescript
// Displays "Apple or Coal"
let rawMessage = {
  translate: "accessibility.list.or.two",
  with: { rawtext: [{ translate: "item.apple.name" }, { translate: "item.coal.name" }] },
};
world.sendMessage(rawMessage);
```
##### ***scoreWildcard.ts***
```typescript
// Displays the player's score for objective "obj". Each player will see their own score.
const rawMessage = { score: { name: "*", objective: "obj" } };
world.sendMessage(rawMessage);
```
##### ***simpleString.ts***
```typescript
// Displays "Hello, world!"
world.sendMessage("Hello, world!");
```
##### ***translation.ts***
```typescript
// Displays "First or Second"
const rawMessage = { translate: "accessibility.list.or.two", with: ["First", "Second"] };
world.sendMessage(rawMessage);
```

### **setAbsoluteTime**
`
setAbsoluteTime(absoluteTime: number): void
`

Sets the world time.

#### **Parameters**
- **absoluteTime**: *number*
  
  The world time, in ticks.

> [!IMPORTANT]
> This function can't be called in read-only mode.

### **setDefaultSpawnLocation**
`
setDefaultSpawnLocation(spawnLocation: Vector3): void
`

Sets a default spawn location for all players.

#### **Parameters**
- **spawnLocation**: [*Vector3*](Vector3.md)
  
  Location of the spawn point. Note that this is assumed to be within the overworld dimension.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> Throws if the provided spawn location is out of bounds.
>
> Throws *Error*, [*LocationOutOfWorldBoundariesError*](LocationOutOfWorldBoundariesError.md)

### **setDynamicProperty**
`
setDynamicProperty(identifier: string, value?: boolean | number | string | Vector3): void
`

Sets a specified property to a value.

#### **Parameters**
- **identifier**: *string*
  
  The property identifier.
- **value**?: *boolean* | *number* | *string* | [*Vector3*](Vector3.md) = `null`
  
  Data value of the property to set.

> [!CAUTION]
> This function is still in pre-release.  Its signature may change or it may be removed in future releases.

> [!WARNING]
> Throws if the given dynamic property identifier is not defined.

#### Examples
##### ***incrementProperty.ts***
```typescript
  let number = mc.world.getDynamicProperty("samplelibrary:number");

  log("Current value is: " + number);

  if (number === undefined) {
    number = 0;
  }

  if (typeof number !== "number") {
    log("Number is of an unexpected type.");
    return -1;
  }

  mc.world.setDynamicProperty("samplelibrary:number", number + 1);
```
##### ***incrementPropertyInJsonBlob.ts***
```typescript
  let paintStr = mc.world.getDynamicProperty("samplelibrary:longerjson");
  let paint: { color: string; intensity: number } | undefined = undefined;

  log("Current value is: " + paintStr);

  if (paintStr === undefined) {
    paint = {
      color: "purple",
      intensity: 0,
    };
  } else {
    if (typeof paintStr !== "string") {
      log("Paint is of an unexpected type.");
      return -1;
    }

    try {
      paint = JSON.parse(paintStr);
    } catch (e) {
      log("Error parsing serialized struct.");
      return -1;
    }
  }

  if (!paint) {
    log("Error parsing serialized struct.");
    return -1;
  }

  paint.intensity++;
  paintStr = JSON.stringify(paint); // be very careful to ensure your serialized JSON str cannot exceed limits
  mc.world.setDynamicProperty("samplelibrary:longerjson", paintStr);
```

### **setTimeOfDay**
`
setTimeOfDay(timeOfDay: number | TimeOfDay): void
`

Sets the time of day.

#### **Parameters**
- **timeOfDay**: *number* | [*TimeOfDay*](TimeOfDay.md)
  
  The time of day, in ticks, between 0 and 24000.

> [!IMPORTANT]
> This function can't be called in read-only mode.

> [!WARNING]
> Throws if the provided time of day is not within the valid range.

### **stopMusic**
`
stopMusic(): void
`

Stops any music tracks from playing.

> [!IMPORTANT]
> This function can't be called in read-only mode.
