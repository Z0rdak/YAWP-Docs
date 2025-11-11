---
title: 'Flag Messages'
description: 'Learn how to customize flag messages (flag alerts).'
sidebar_label: 'Messages'
sidebar_position: 2
sidebar_custom_props:
  customEmoji: 📨
---

## Flag messages

Flags have their own dedicated flag message which is shown when the flag is triggered. Further it's now possible to mute flag messages for each individual flag (disabling the alert of the region will still mute
all flags for the region).

Use the following placeholders (starting with 0.6.1-beta1) in flag messages to refer to specific region info:
* `%1$s` - flag name
* `%2$s` - position of the flag action ( \[X=x, Y=y, Z=z\] )
* `%3$s` - region name involved in the flag check
* `%4$s` - dimension name
* `%5$s` - player name involved, if applicable
* `%6$s` - team name involved, if applicable
* `%7$s` - the group name involved, if applicable
* `%8$s` - entity name involved, if applicable
* `%9$s` - block name involved, if applicable

Flag messages also can be formatted by using the minecraft default string formatting.
* For example `&c %5$s &r tried to break a block in &9 %3$s &r!` will result in a red player name and a blue region name.
* Take a look at [this tool](https://codepen.io/0biwan/pen/ggVemP) for reference as well as the [minecraft wiki](https://minecraft.wiki/w/Formatting_codes).

There are default flag messages defined for each player related flag in the resource pack (internationalization) which can be customized.

There are also suggestion flag messages defined for the CLI in the resource pack which can be customized.

***
## Interactive CLI

When managing the flags of regions you will most likely use the flag list command. This command will show you an interactive list of all flags of the region. You can then click on the flag name to get more information about the flag and to change the flag state.

![flag-list](../img/cli-region-info-flags.png)


