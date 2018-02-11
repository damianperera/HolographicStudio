# Before you Build
- The project depends on the _ProEnsembleCalibrationLib_ that is part of the [RoomAlive Toolkit](https://github.com/Kinect/RoomAliveToolkit), download and build that project first and update the reference to that library.
- Both this project and RoomAliveToolkit reference the same _SharpDX_ libraries, make sure that the used libraries reference the same version of these libs to prevent conflicts.

# Calibration 
The application needs a calibration XML file that can be created with the _CalibrateEnsemble_ application that is part of RoomAlive Toolkit. For more details read the instructions on the RoomAlive Toolkit project page. 

HolographicStudio needs to be configured to find the resulting calibration file. Use the _EnsembleConfigurationFile_ application configuration entry to point it to the location of your calibration file. Note that it expects the file to be placed in a location under the Public Documents folder.

# Running Holographic Studio
Before running the application make sure that the _KinectServer_ is running on each PC with a Kinect attached.

## Controlling the camera

Use the *W*, *A*, *S*, *D*, keys to change the orientation of the camera.
The *E* and *C* keys can be used to change the zoom factor.

## Tweaking parameters

Use the *T* key to toggle the display of a parameter editor.
The *←* and *→* arrow keys walk through all available parameters.
The *↑* and *↓* arrow keys change the value of the parameter.
Hold *shift* while pressing *↑* and *↓* keys to increase the stepsize.

* ### Clip Radius
Clips the scene when the distance to the center is larger than this value.

* ### Clip CenterX   
Moves the clip center to left or right wrt to first Kinect in the ensemble.

* ### Clip CenterY      
Moves the clip center up or down wrt to first Kinect in the ensemble.

* #### Clip CenterZ   
Moves the clip forward or backward down wrt to first Kinect in the ensemble.

* ### Clip Floor        
Sets the bottom Z for clipping.

* ### Clip Ceiling 
Sets the top Z for clipping. 

* ### Apply Holographic Effect
Toggle the shader to apply a holographic effect.

* ### Animate         
Automatically rotates the camera. For each Kinect in the scene there will be a parameter with the index of the camera appended.

* ### LiveDepth     
Toggles live depth updates.

* ### LiveColor 
Toggles live color updates.

* ### FilterDepth
Toggles depth filtering.

* ### SpatialSigma
The spatial sigma for depth filtering.

* ### IntensitySigma
The intensity for depth filtering.

* ### DepthThreshold
Threshold for discarding triangles based on steepness.

