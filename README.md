# Obj2CityGML
Obj2CityGML is a full-stack app which enables to converting OBJ 3D models with semantics to CityGML LOD1-4 with ease. It allows for high-performance conversion between 3D OBJ models and CityGML LOD1-LOD4.Also, in this app users can display models correctly on Cesium.js platform.
- convert OBJ models to CityGML LOD1-4
- convert OBJ models to GLTF
- display models in Cesium.js platform by model's seven parameters
>seven parameters : model location(longitude, latitude, height or altitude), model orientation(rotation around X,Y,Z axis), and model scale. PS: model coordinate system is based on the `north-east-up` reference frame.

- login/signup 

# Overall design
## Architecture
to draw

## UI design
to draw

## Technology
- postgresql
- node.js,express.js and some related node modules, like obj2gltf,pg-promise
- bootstrap,jquery,angular
- FMEServer.js, FME Rest API
- FME Desktop

## Obj with semantics
Obj models donot contain any semantic infomation which indicates the plane's semantics like floor,window,door,ceiling,wall and etc.
In this app, Obj models to be converted should add some semantics which can be stored in texture information.For example,following code demonstrates two planes; The first plane is labled with FLOOR semantics while another plane is labled with CEILING semantics. NOTE: the semantics string should kept aligned with CityGML building semantic type,like FLOOR,CEILING,WINDOW,DOOR,WALL,FURNITURE and etc.

excerpt of an Obj model.
```
g FLOOR g
usemtl FLOOR
f 15 1 19
f 15 7 1
...

g CEILING g
usemtl CEILING
f 16 2 20
f 16 8 2
...
``` 

# Todos
- convert OBJ models to CityGML LOD1-4
- convert OBJ models to GLTF
- display models in Cesium.js platform by model's seven parameters
- login/signup 

# License
Obj2CityGML is licensed under the Apache License, Version 2.0. See the LICENSE file for more details.

