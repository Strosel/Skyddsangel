# Skyddsangel

A VR test platform for evaluating the user experience of drone based lighting solutions developed with Unreal Engine 4.
[Thesis](./)

## Usage
Currently Unreal Engine is required to run the project. 

To start a session use the `VR Preview` in UE. This will start two instances, one in VR and one local on the PC. To move forward or backward the vr player can use the triggers on their controller

### Runtime Parameters
During runtime one can modify some of the drones parameters via a heads-up-display.
These parameters are as follows:
 - Altitude above the VR user
 - The horizontal distance from the VR user
 - Light angle
 - Light intensity
 
### Other parameters
Other parameters of interest and where to modify them are detailed below.

#### Noise volume
The volume of the noise produced by the drone is of course relative to the distance between it and the VR player. If a maximum of minimum volume different to that of the default is desired it can changed by modifying the `Max Volume` and `Min Volume` variables in the `DronePawn`.

#### Environment darkness
The environment darkness is produced by three different sources, a sky sphere, a directional light and a post processing volume. Each can be modified on their own to produce the desired darkness and effect.

#### User speed
The player speed along the track can be changed by modifying the `Speed` (in km/s) variable in the `DronePawn`.

#### Track path
If a new track path is desired in any environment one can drag the `Track` actor into the level editor and use it to draw a new path. To select this new track, give the new instance a tag in the properties pane and then set the `TrackTag` variable in `2PGameMode` to that same tag.
