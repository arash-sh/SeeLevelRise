# See Level Rise 
Esri's Intern Hackathon 2022


## **Abstract**
Human-induced climate change is causing sea level rise and exacerbating extreme weather events, increasing the magnitude and frequency of floods. Despite worsening floods globally, there exist many misconceptions about flood risk in the United States. We want to translate flood risk in a way that makes it no longer ignorable, but also to provide people with the resources they need to take action. There is a large gap between the total number of Americans facing flood risk and the number of Americans with flood insurance, so we want to encourage people to find coverage to prepare them for the inevitable. 

## Introduction
Our app immerses users into a 3D model of their city, allowing them to simulate flooding events, discover risk, and estimate damages. With a sliding bar, users can visualize the reach and magnitude of different flooding levels. Another pane shades buildings in your city according to flood risk as determined by the Federal Emergency Management Agency (FEMA), so users can see their risk relative to other parts of their city. A third pane allows users to click on buildings in the city and receive an estimate for the cost of flooding damages, with a link to an insurance premium calculator if they would like to receive a quote.  We also provide in-app resources for learning about the flooding with the hope of dispelling common misconceptions and empowering users to protect themselves with flood insurance. 

## Implementation
We built See Level Rise using the newly released ArcGIS Maps SDK for Game Engines. Using the Unreal Engine, we incorporated floodplain, sea level rise, and building height data to visualize how different water levels will impact New York. 

To shade buildings according to flood risk, we completed a series of spatial joins of the open-source New York footprint layer with the flood risk layer in ArcGIS Pro, using the extrude tool to convert the model to 3D.  We then exported this to CityEngine, where we could add detail and shading. From here we exported the model to UnReal to be incorporated as a feature of our app. 

This app was made using the ArcGIS Maps SDK for Game Engines version 1.0.0.

## Usage
This app requires the ArcGIS Maps SDK for Unreal Engine, which can be downloaded [online](https://developers.arcgis.com/unreal-engine/). Place the SDK in a folder called Plugins within the project folder. 

 - Hold the right mouse button and **WASD** keys for motion. 
 - For the Sea Rise Visualization, use the left mouse button to interact with the slider.
 - For the property damage estimate, use the middle mouse button to select the buildings.

## What's Next

We hope to extend the capabilities found in See Level Rise to cities across the U.S. We would also like to add more precision to our cost estimates. A lot more data exists for flood risk and damage estimations at residential buildings than for commercial properties. Bridging this information gap will improve the accuracy of our model and make it indispensable for property owners. 
