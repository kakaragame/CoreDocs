# The Basic Mod Example

### Please read [mod.json](/creatingmods/mod-json) first.


## Main Class


### Loading Stages
A loading stage is a stage during a mod load that you can do add different things to the game such as Items, Entities, or World Generators.  This is not the only time you may load your these items. This is just a simple way to manage the different parts of the code
#### Default Loading Stages

|ClassName| Description  |  
|--|--|
|`org.kakara.core.game.ItemManager`  | At this stage you will be able to register any Items you have  |  

### Using the LoadingStage
Inside your main class you will want to create a method and add the annotation
`@LoadingStage`
Example
```java
  @LoadingStage
  public void worldGenLoad(WorldGenerationManager worldGenerationManager) {

  }
```

## Resource Layout
Resources are laid out inside in a specific way. This way Kakara can load them automatically with no custom extra code to the user.

Inside the base of your mod you will have a resources folder.
Depending on the type they will be laid out inside a special way.
### Textures
  Textures have the most rules due to texture details.
  Inside your resources folder you will have a textures folder. And inside that you will have a folder for each Texture Resolution. 16,32, [ect](https://github.com/kakaragame/core/blob/master/core/src/main/java/org/kakara/core/resources/TextureResolution.java).
  Within that folder you can call organize it anyway you want..
  Here is an example.

  ```
  resources/textures/16/tools/stone/stone_pickaxe.png
  resources/textures/16/tools/stone/stone_axe.png
  resources/textures/64/tools/stone/stone_pickaxe.png
  resources/textures/64/tools/stone/stone_axe.png
  ```
