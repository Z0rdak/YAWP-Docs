---
title: 'Inheritance.. what?'
description: 'Dive into the advanced topic of flag inheritance.'
sidebar_label: 'Inheritance'
sidebar_position: 3
sidebar_custom_props:
  customEmoji: 👨‍👨‍👦
---

## Flag inheritance

Version 0.0.4.0-beta1, introduced flag inheritance. This means that flags are inherited from parent regions to child regions.

- The same flag set in a child region will take precedence over the same flag of any parent region in flag checks.
  This means that if a flag is set in the parent region, the child region can override this flag by setting it to a different value. If a flag is not set in the parent region, the child region can set it to a value.

_Remember that child regions must have a higher priority than their parent regions._

- If a flag is set in the parent region, but not set in the child region, the flag will be inherited from the parent region.

- A parent region can set its flags to override the flags of all child regions. This means that the child regions can't override the flag set in the parent region.

The following table show how flags are handled for region hierarchies. Note that n/a here represents a disabled flag or an undefined flag state:

| Parent                |  Child  | Result  |
|:----------------------|:-------:|:-------:|
| Denied with override  |   Any   | Denied  |
| Allowed with override |   Any   | Allowed |
| Denied                | Denied  | Denied  |
| Denied                | Allowed | Allowed |
| Allowed               | Denied  | Denied  |
| Allowed               | Allowed | Allowed |
| n/a                   | Denied  | Denied  |
| n/a                   | Allowed | Allowed |
| Denied                |   n/a   | Denied  |
| Allowed               |   n/a   | Allowed |
