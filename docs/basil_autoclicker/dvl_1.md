## Devlog 1


## How do we imitate a human? <!-- {docsify-ignore} -->

#### We don't consistently click the same CPS. <!-- {docsify-ignore} -->
At higher CPS values (8+), it becomes very hard to keep your CPS at a steady, non-volatile value.

Due to our inability to do so, many anticheats can see a steady, unchanging CPS, and flag that for being *most likely* not human.

So, the first step into tricking an anticheat into thinking the user is naturally clicking, we can simulate:

1. Jittering
    - This means that the user's CPS will fluctuate up and down depending on some element of randomness
2. Click trends
    - This means that the user's CPS will follow a randomly chosen descent or ascent, at intervals

#### We **cannot** consitently click at the same interval. <!-- {docsify-ignore} -->
What do I mean by this? Well, each time you click, you click at an interval from the previous click, this will, or should always be sufficiently different.

Due to this inability to constantly click at the same interval (in millisecond terms), many anticheats can see that, and flag for an autoclicker.

To bypass this, we can add a random offset to the interval between each click.

#### We do not click for exactly the same interval. <!-- {docsify-ignore} -->
While this is mostly visible clientside, it still helps make the player look more legitimate.

This is also easily fixed, as we can just put a random interval between click and release, with a range of something like 5 - 15 milleseconds.

#### What does this look like all put together? <!-- {docsify-ignore} -->
[Check this *Youtube video*](https://youtu.be/RwHxlEpQG1w)

> NOTE: DVL 1, Last updated (8/31/2021) by basilicous, STATUS : [MORE EXPECTED IN SERIES]