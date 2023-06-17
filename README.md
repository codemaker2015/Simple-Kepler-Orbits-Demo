# Simple Kepler Orbits Demo

Unity3d project for simulating simple orbits using 2-body solution model.

![gif](Demos/demo1.gif)
![gif](Demos/demo2.gif)


#### Initializing orbit from orbit elements (JPL database supported)
```cs
	var body = GetComponent<KeplerOrbitMover>();
	body.AttractorSettings.AttractorObject = attractorTransform;
	body.AttractorSettings.AttractorMass = attractorMass;
	body.AttractorSettings.GravityConstant = GConstant;
	body.OrbitData = new KeplerOrbitData(
		eccentricity: eValue,
		semiMajorAxis: aValue,
		meanAnomalyDeg: mValue,
		inclinationDeg: inValue,
		argOfPerifocus: wValue,
		ascendingNodeDeg: omValue,
		attractorMass: attractorMass,
		gConst: GConstant);
	body.ForceUpdateViewFromInternalState();
```

#### Initializing orbit from orbit vectors
```cs
	var body = GetComponent<KeplerOrbitMover>();
	body.AttractorSettings.AttractorObject = attractorTransform;
	body.AttractorSettings.AttractorMass = attractorMass;
	body.AttractorSettings.GravityConstant = GConstant;
	body.OrbitData = new KeplerOrbitData(
		position: bodyPosition, 
		velocity: bodyVelocity, 
		attractorMass: attractorMass, 
		gConst: GConstant);
	body.ForceUpdateViewFromInternalState();
```

For more detailed scripting snippets go to the [included manual](Assets/SimpleKeplerOrbits/Readme.md).

## Package version

[Unity Asset Store]: https://assetstore.unity.com/packages/tools/physics/simple-kepler-orbits-97048