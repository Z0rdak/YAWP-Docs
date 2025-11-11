---
title: 'Local Region concepts'
description: 'Local Region, Claim, Plot - different names for the same thing.'
sidebar_label: 'Local'
sidebar_position: 4
sidebar_custom_props:
  customEmoji: '🏡'
---

With Local Regions you are able to define areas in your world, which you want to protect from certain actions/events, 
which are caused by players, other entities or the environment.

The area of a region is defined by a Cuboid shape (more shapes are planned for the future!). They also have a priority to manage overlapping regions.

The flags defined in the region only work in this confined area. The properties of Local Regions, 
which distinct them from the other region types are described below.

![](../img/cli-local-region-info-overview.png)

***
## Area Properties

![local-region-area](../img/cli-local-region-info-spatial.png)

The Area Properties of a region describe the area the region is restricted to, the teleport position, 
the marked blocks to define the region area and lastly the type of the area.

The AreaType defines the shape of the region. The currently supported shapes are Cuboids and Spheres. 
Future updates will bring more AreaTypes like Cylinder, Prism and Polygon shapes.

### Shape definitions

- Cuboid areas are defined by marking/supplying the diagonal opposite corner blocks.
- Sphere areas are defined by marking/supplying the center block and the radius of the sphere.

The teleport position is automatically set when defining a region. This is a default value, which is the center of the area. 
It can be overwritten with the command `/yawp region <dim> <region> tp set <Block>` and teleport to by using `/yawp region <dim> <region> tp set <Player>`.

### Related [Commands](../../commands/region/local-commands)

- [Creating a region](../../commands/region/dimension-commands#creating-a-region-with-the-cli)
- [Expanding the area](../../commands/region/local-commands#area-commands)
- [Setting the area](../../commands/region/local-commands#area-commands)
- [Setting the teleport position](../../commands/region/local-commands#area-commands)

***
## Overlapping regions

Beside having child regions, you will sometimes have overlapping regions which are not directly related as parent or child. 
These overlapping regions do need to have different priorities to work properly.

If a region is overlapping with another region, you'll need to adjust the priority for them to make the flags work properly.

**The higher the number, the higher the regions' priority.**