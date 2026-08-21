# 2D Unet CXR mask training, prediction, deep-feature classification and explanation
install the conda virtual environment
```
conda create --name 2D-seg python=3.10 conda-forge::albumentations==2.0.5 conda-forge::segmentation-models-pytorch grad-cam seaborn shap
```
the output is just a demonstration of how the result will look like, it is not the result expected
Dataset: https://www.kaggle.com/datasets/kmader/pulmonary-chest-xray-abnormalities
the mask of this set is predicted from a model I trained earlier on another dataset