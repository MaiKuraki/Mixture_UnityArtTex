# Changelog
All notable changes to this project template will be documented in this file.

## 0.4.3

Add compatibility for Unity 6 and above.

## 0.4.2

### Added
- Cloud layer encode / decode nodes.

### Fixed
- Fixed random color node not using the correct random system.

### Changed
- Random Range node now output a vector instead of a float.

## 0.4.0

### Added
- Earth Heightmap node, directly fetches real world height data into a texture.

https://user-images.githubusercontent.com/6877923/123006036-64e2e780-d3b7-11eb-922e-018994b32da5.mov

- Added conversion methods for Vector3 and Vector2 to Vector4.
- Added a popup to select which preview texture is visible in the output node.
- Added an option in the self node to select the output texture.
- Added a Vector Field node to generate simple vector field patterns.
- Added a button in the toolbar to restart a realtime effect.
- Added a vector field preview mode in the Preview node.
- Added total processing time in realtime mixture output node.
- Added support of cubemap in the node inspector.

https://user-images.githubusercontent.com/6877923/124649079-535e0d00-de98-11eb-9e85-13c3a5d987ca.mov


- Added an option to select the density channel in the node inspector volumetric preview.
- Added an option to invert the surface in the node inspector SDF preview.
- Added a tileable curl noise option.
- Added a dedicated cylinder node instead of reusing the line node.

### Fixed
- Fixed missing nodes in the list of nodes proposed when dragging an edge.
- Fixed gamma mismatch when exporting a 2D texture with the External Output node.
- Fixed incorrect create node list when opened from an edge.
- Fixed processing of nodes not connected to the output in realtime mixtures.
- Fixed a setting inheritance bug when a node inherited from a Texture node.
- Fixed migration of old mixture graphs to the new settings system.
- Fixed preview node not showing pixel value
- Fixed the rounding in frequency and lacunarity of noise nodes.

### Changed
- Blur now works with percentage rather than pixels

## 0.3.0

### Added
- Mirror Node

![image](https://user-images.githubusercontent.com/6877923/114311850-b554e380-9af0-11eb-896d-46df72f6e06e.png)
- Particles Node (Experimental)

https://user-images.githubusercontent.com/6877923/115990868-e8ee3e00-a5c5-11eb-9467-ef8470e74066.mp4
- Curl Noise (divergence free noise)
- Added an "initial texture" input for the self node.
- Added a Vector To Texture node, similar to the Color To Texture node but takes a vector as input.
- Polygon node (generate 2D distance field shapes)
![image](https://user-images.githubusercontent.com/6877923/120940697-d287e600-c71e-11eb-9505-a15b3d5befa8.png)

### Changed
- Separate Node now keeps the separated texture channels in their respective channels (G -> G instead of G -> R) but takes 4 times more memory.
- Added an option in the Blend node to remove negative values.
- Completely refactored how settings are working in graphs.
- The node inspector preview settings are now serialized per graph within the editor session (not saved between sessions).
- Texture, Shader, Compute Shader, Mesh and Prefab Capture nodes are now renamable.
- You can directly drag and drop Texture, Shaders, Compute Shader and GameObject into the graph to create nodes.

### Fixes
- Fixed the internal texture filter mode of the gradient node when using "Fixed" gradient mode.
- Fixed mixture when text Mesh Pro is installed
- Fixed sRGB copy issues with the self node.
- Fixed graph inconsistencies related to undo-redo.

## 0.2.1

### Fixed
- Fix an issue with the new Input System when adding the Mixture package
- Fixed an error with the build
- Fixed the scale and bias node in 3D

## 0.2.0

### Added

- Stochastic Tiling node  
![StochasticTiling](https://user-images.githubusercontent.com/6877923/106679862-c4ce2280-65bd-11eb-87bb-eee4d88b1e2c.gif)
- Discretize Node  
![image](https://user-images.githubusercontent.com/6877923/106681232-63f41980-65c0-11eb-89a5-39468b746d89.png)
- Preview Node
![image](https://user-images.githubusercontent.com/6877923/107294139-2df5e000-6a6d-11eb-9b71-c21cf7e91072.png)
- Difference Node
![image](https://user-images.githubusercontent.com/6877923/107442526-82fe2880-6b37-11eb-888a-e59d6470af5b.png)
- Swap Color Node
![image](https://user-images.githubusercontent.com/6877923/113365427-8606df80-9356-11eb-8dea-aca8ec17acd1.png)
- Separate Node
![image](https://user-images.githubusercontent.com/6877923/113365441-9454fb80-9356-11eb-96ae-9efea54ce595.png)
- Contrast Node
https://user-images.githubusercontent.com/6877923/113365470-ab93e900-9356-11eb-90b7-2dc38c66f8e4.mp4
- Added Rasterize 3D mesh node
![image](https://user-images.githubusercontent.com/6877923/113605649-3e7a9f00-9647-11eb-9ddb-67f25ec01225.png)


### Changes
- Improved Generate MipMaps node (added a mode to select which kind of mipmap generation you want + a custom option with a shader)
- The custom mipmap shader option was removed from the output node settings, but now if an input texture has mipmaps and the mipmaps are enabled on the output, they are copied (instead of being re-generated by the output node).
- Added the possibility to have custom mipmap for 3D and Cubemap textures with the Generate MipMap node directly connected to the Output.
- Improved the support of 3D texture preview in the node inspector, now volumetric and SDF views are available.
- Renamed Mesh to UDF node into Mesh to SDF and added an option enabled by default to generate SDF from meshes. 

## 0.1.0

### Added
- Mixture Variants
https://user-images.githubusercontent.com/6877923/105640496-b164de00-5e7e-11eb-921f-95093e411c86.mp4
- Object To Map node
![image](https://user-images.githubusercontent.com/6877923/105640618-45cf4080-5e7f-11eb-88b6-6c26616b4af8.png)
- Generate MipMap node
![image](https://user-images.githubusercontent.com/6877923/105640649-71522b00-5e7f-11eb-941f-5d757a22f3a4.png)
- Added a debug menu to directly access shader/compute shader code and node documentation from the context menu
![image](https://user-images.githubusercontent.com/6877923/105640719-b37b6c80-5e7f-11eb-8bfb-843c4129ebd5.png)

## 0.0.5

### Added

- Transform node  
![](docs/docfx/images/TransformNode.gif)
- UV input for procedural shapes  
![image](https://user-images.githubusercontent.com/6877923/99877502-f65e6100-2bfe-11eb-9851-ac879192c7f7.png)
- CubeMap compression settings  
![image](https://user-images.githubusercontent.com/6877923/100515883-bd366b80-317f-11eb-9f01-b3628be6463d.png)
- Levels node with histogram view  
https://user-images.githubusercontent.com/6877923/102899157-ca870300-446a-11eb-8b8e-4822bb48d608.mp4
- Highlight nodes when hovered in the node inspector  
![Highlight](https://user-images.githubusercontent.com/6877923/102915192-aa167300-4481-11eb-8ea4-67fa8c173a79.gif)
- UV input for procedural shape nodes  
![image](https://user-images.githubusercontent.com/6877923/102915073-7dfaf200-4481-11eb-8b5c-d8006743aced.png)
- A bunch of fractal nodes  
![image](https://user-images.githubusercontent.com/6877923/102915300-d8944e00-4481-11eb-8e93-f7a57c21b830.png)
- Volume to Vector field node  
- Compression for Cubemap mixtures  

### Changed
- Better SRGB management  
![image](https://user-images.githubusercontent.com/6877923/102915118-8f43fe80-4481-11eb-827d-6504a32b33b4.png)
![image](https://user-images.githubusercontent.com/6877923/102915158-9bc85700-4481-11eb-8a46-d60f4989d005.png)
