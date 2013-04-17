Lightning Generator for CINEMA 4D
======================

>A Python generator for creating lightning effects in CINEMA 4D.

#[Download](https://github.com/CreativeTools/ct-lightning-generator/raw/master/ct_lightning_generator.c4d)

##File contents

The C4D file contains a number of objects:
* Sweep NURBS
    * Circle
    * CT Lightning Generator
        * Target
        * Source

_CT Lightning Generator_ is the actual lightning generator, the others can be replaced by your own objects.
_CT Lightning Generator_ generates a spline containing a segment for each "branch" in the lightning bolt.

##Settings
The _CT Lightning Generator_ object has a number of settings in the _User Data_ tab.

* Step size
    * The distance between the points in the spline. A smaller value creates more details while a larger walue will give the bolt a rougher look
* Source Object
    * The object to use as the starting point for the lightning bolt. Note that it only uses the axis center of the object.
* Target Object
    * The object to shoot the bolt towards. Just like with the source object, only the axis center of the object is used.
* Branch Length
    * The distance the branches should be allowed to extend from the main bolt.
* 2D
    * When checked the bolt will be "flat". This makes sure that the branches never look like they're overlapping.
* Branches
    * The amount of branching from the main bolt. A low value will disable branches entirely.
* Random Seed
    * Each random seed gives you a new variation of the bolt. Animate this to generate rapidly changing sparks.
* Max Steps
    * The maximum number of steps the generator should take when generating the bolt. Raise this if the bolt does not reach the target object. Note that the generation time is proportial to the square of the number of steps, so be careful with this setting!
