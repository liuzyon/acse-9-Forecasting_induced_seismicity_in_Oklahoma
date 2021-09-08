This project have four folders, which are list in below:

###### src

This directoy contains three files.

- feature_extraction.ipynb: Import meta data from industry and geological files in *datasets* directory and generate dataset for models' use according to gridding and stored it in *data* directory.
- models_construction.ipynb: Implement the stepwise regression with VIF checking to select features,
  construct logistic regression model and neural network model and analysis their performance.
- visualization.ipynb: This is used for generating some figures in report, which is not code of project implementation.

###### data

This directory stored the dataset files generated from feature_extraction.ipynb, which are used for model training.

- 2011-2018_40*40_rectangular_mode_features.csv: the dataset file generated in feature_extraction.ipynb. It will be used in models_construction.ipynb

###### datasets

Because githhub only support small size files and datasets files can not be uploaded, so we upload it to onedrive and you can download them to run code: 

**https://imperiallondon-my.sharepoint.com/:u:/g/personal/zl1220_ic_ac_uk/EXRa_WZhTXBBlgE48eRUtqABL249FkWWpZSRam1qief8oQ?e=9xb4Oj**

This directory stored meta data of seismicity, industry and geological formation. It contains injections, earthquakes, hydraulic fracturing, wells and geological data.

###### model

This directory stores trained  logistic regression model and neural network model file, which can be reloaded.



## How to run the project

1. First download the datasets by the

   **https://imperiallondon-my.sharepoint.com/:u:/g/personal/zl1220_ic_ac_uk/EXRa_WZhTXBBlgE48eRUtqABL249FkWWpZSRam1qief8oQ?e=9xb4Oj** 

   Unzip it, note it should be a directory called datasets and placed in root project directory as other folders ( src, data, model)

2. Run the feature_extraction.ipynb cell by cell

3. Run the models_construction.ipynb cell by cell

You will see one run of whole procedures in this project.
