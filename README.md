# Operational Research in Solar Energy
This repository goes over 2 projects:
1. Irradiance Dynamic Heatmap
2. Solar panel image recognition

In case The jupyter notebooks cannot be previewd in github, but to run you could open it through google colab or in a local jupyter notebook intepreter


## Irradiance Dynamic Heatmap
This python notebook goes through how to extract data from the coppernicus database. To start you would need to make a coppernicus account and recieve the API key.
To get the key, open https://ads.atmosphere.copernicus.eu/profile and copy the API key into the 2nd Cell of the notebook `Irradiance_Dynamic_Heatmap_Tutorial.ipynb` at the `coppernicus_key` variable.

Data source:
- Irradiance data: https://ads.atmosphere.copernicus.eu/datasets/cams-gridded-solar-radiation
- Temperature data: https://ads.atmosphere.copernicus.eu/datasets/cams-global-reanalysis-eac4-monthly

The final results woud be a dynamic heatmaps such as
![](/images/heatmap_GHI.png)

## Solar panel image recognition
Solar panel image recognition using the YOLO model through the Roboflow server.

To start you would need to make an account and project in Roboflow: https://app.roboflow.com/.
Inside of Roboflow you'll need to setup a new online annotated image dataset.
1. upload the images in `/original_dataset` that will be used to train the model. 
2. select and make a category of the object that needs identification and select it for the model to identify.

![](/images/roboflow-annotate.jpeg)
4. separate the images into training set, validation set, and test set (70%-15%-15% split)
5. 
![](/images/roboflow-dataset.jpeg)
6. Copy the dataset key and then open the jupyter notebook `solar_project_panel_detection.ipynb`
7. run the model and check the results

![](/images/Yolo-Result.jpeg)


My google colab code:
Heatmap: [https://colab.research.google.com/drive/1OSbH1QFRAnpgIwXDDmk8_zap0tEFk9Ou?usp=sharing]
Image-recognition: [https://colab.research.google.com/drive/1rGhPuab-VQQFZt39sxPTwOPPFqh4hM8J?usp=sharing]
