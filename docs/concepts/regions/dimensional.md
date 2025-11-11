---
title: 'Dimensional Regions'
description: 'Dimensional- or Level-Region, its the same.'
sidebar_label: 'Dimensional'
sidebar_position: 3
sidebar_custom_props:
    customEmoji: 🗾
---

Dimensional Regions are a special kind of regions because they have no spatial restrictions.
Dimensional Regions work like normal regions, but are tied to a dimension.

They can have owners, members, flags and can be activated and deactivated.

![dim-info](../img/cli-dim-region-info.png)

## Creation

Dimensional Regions **can't** be created manually. They are in fact automatically generated with each new dimension. 
The first Dimensional Region for the overworld is created when the server is created.

The following Dimensional Regions are created whenever a player travels to a new dimension, 
thus creating the new dimension with their respective Dimensional Region.

![dim-regions](../img/cli-dim-region-info-regions.png)

## Managing & [Commands](../../commands/region/dimension-commands)

Dimensional Regions can be managed only by their owners, or by players which have the
required [permission](../../config/permissions).

Members will only bypass flags, like owners do. Note that even with the permission from the config, 
you won't be able to bypass flags when you are not a member or an owner of a region.

To manage Dimensional Regions, just use the `/yawp dim <dim>` command. Where `<dim>` relates to the registry name of the dimension. 
E.g. for the overworld this would be `minecraft:overworld`, for the nether `minecraft:the_nether` and `minecraft:the_end` for the end dimension.
But any other dimension either added by a mod or a data pack should work the same way.

