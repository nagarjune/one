# Crowd crisis movement simulation for the ONE [![Build Status](https://travis-ci.org/davidsan/one.png)](https://travis-ci.org/davidsan/one)


A fork of the Opportunistic Network Environment simulator (the ONE) featuring crisis crowd movement.

Generated Javadoc can be found at : [https://davidsan.github.io/one](https://davidsan.github.io/one).

Repository can be found at : [https://github.com/davidsan/one](https://github.com/davidsan/one).

For more information on the ONE, visit [http://www.netlab.tkk.fi/tutkimus/dtn/theone](http://www.netlab.tkk.fi/tutkimus/dtn/theone).


## Implementations
### Crowd movement
Crowd movement is implemented with the `DangerMovement` class and his sub-models (`EvacuationCenterMovement`, `HomeMovement`, `RandomPathMapBasedMovement`, `ShortestPathMapBasedPoiMovement`, `SosMovement`).

### Closed roads
Closed roads are implemented using `AccidentGenerator` which generate `AccidentEvent`. Those events make changes to the `MapNode`'s instances by calling the close() method.


## Changes
This fork is based on version 1.5.1 RC2 of the ONE.

### New classes added

* `movement.DangerMovement`
* `movement.EvacuationCenterMovement`
* `movement.HomeMovement`
* `movement.RandomPathMapBasedMovement`
* `movement.ShortestPathMapBasedPoiMovement`
* `movement.SosMovement`
* `movement.map.PointsOfInterestEvac`
* `input.EmptyEvent`
* `input.AccidentEvent`
* `input.AccidentGenerator`

### Existing classes edited
* `core.Coord` : changes on distance methods
* `movement.map.MapNode` : adding new property for closed map node
* `gui.playfield.NodeGraphic` : for coloring the node according to the movement model
* `gui.playfield.MapGraphic` : for coloring the road closed

## Example of scenario
An example of scenario can be found in the `danger_settings.txt` file.


## Authors
* Virginie Collombon (`virginie.collombon {at} gmail.com`)
* David San (`davidsanfr {at} gmail.com`)
