# Rock Classification using CNN
Classify six types of rock using a Convolutional Neural Network.

## Prologue
Rock classification is a fundamental part of geological surveys. However, accurate classification of rock is still challenging considering the high variety of rock types and the nonuniformity of their properties. Therefore, I present a method to classify six types of rocks. 

# What It Is
This project can classify high similarity six types of rock with accuracy of 93% and show the results with a saliency map highlighting the discriminative object parts detected by the CNN.


# Dataset
The [SDNet2018](https://digitalcommons.usu.edu/all_datasets/48/) dataset is the benchmark for crack detection which contains over 56,000 images of six types of rock: cracked and uncracked concrete bridge decks, walls, pavements, respectively. The dataset includes cracks as narrow as 0.06 mm and as wide as 25 mm with a variety of obstructions, including shadows, surface roughness, scaling, edges, holes, and background debris. Each image is segmented into 256 *256 pixels sub images for later uses.


# How It Works
## Generation of custom cylinder
1. Right click on Unity and select Create/CylinderData

2. Set parameters for generation of cylinder
    - **material**  
      the material of cylinder
    - **circle resolution**  
      the number of vertices of circle meshes
    - **height resolution**  
      the number of vertices of height meshes
    - **spatial resolution** [m/vert]  
      the length per one vertex
    - **smooth texture**  
      refine uv-mesh in connection of vertices
    - **sommth normal**  
      refine normal vector in connection of vertices
    - **generate zenith**  
      if true, generate zenith (top of cylinder)

<p></p>

3. Click "Save" and "Generate" botton to generate cylinder object  
  Note that: Game object in scene and asset correspond to each other. Therefore, if you want to create the other, create new CylinderData.

4. If parameters change, click "Update" botton

## Generation of custom camera arrangement
1. Right click on Unity and select Create/CylinderCameraData

2. Set parameters for camera arrangement
    - **cylinder data**  
      target cylinder data asset for shooting
    - **position offset** [m]  
      the offset of camera arrangement (0 m means same height with zenith)
    - **sampling resolution** [/s]  
      shooting resolution per second (frame per second)
    - **camera velocity** [m/s]  
      the falling velocity of camera
    - **camera rotation velocity** [euler/s]  
      the rotation velocity of camera (euler angle)
    - **render size**  
      output image size
    - **render path**  
      output images path

<p></p>

3. Click "Save" and "Generate" botton to generate camera objects  
  Note that: Semilar to cylinder, game object in scene and asset correspond to each other. Therefore, if you want to create the other, create new CylinderCameraData.

4. If parameters change, click "Update" botton

5. Click "Render" botton to shoot images  
  It may be several seconds. The output images will be generated in render path.


# Author
- Yuki Sakamura
- sakamura.yuki@image.iit.tsukuba.ac.jp
- Computer vision and image media lab.
