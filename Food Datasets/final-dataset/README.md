# About

This folder contains the final dataset (after preprocessing Recipes5k, Nutrition5k, Food101).

## Getting Started

### Prerequisite

- Downloaded all the datasets and are stored in their respective directories

### Installation

1. Navigate to _USDA-FNDDS_ directory and execute **create_ingredients_database.ipynb**

   ```
   cd ../USDA-FNDDS
   ```

2. Navigate to _recipes-5k_ directory and execute **preprocess_recipes5k.ipynb**
   ```
   cd ../recipes-5k
   ```
3. Navigate to _food-101_ directory and execute **preprocess_food101.ipynb**
   ```
   cd ../food-101
   ```
4. Navigate to _nutrition-5k_ directory and execute **preprocess_nutrition5k.ipynb**
   ```
   cd ../nutrition-5k
   ```
5. Upon completion, the root directory of final-dataset should look like below

   ```
   |- images
   |- metadata
   |- README.md
   ```

   - **images** will contain 101 subdirectories, each represent a food category filled with >= 100k images.
   - **metadata** will contain csv files that stored the nutrition and ingredients data for each dish of every category. Metadata of each dataset is stored separately.

6. Navigate to _main_ directory and execute **data_pipeline.ipynb**
   ```
   cd ../../main
   ```
7. Upon completion, the root directory of final-dataset should look like below

   ```
   |- images
   |- metadata
   |- tfrecord
   |- README.md
   ```

   - **tfrecord** contains the serialized version of Food-101, Recipes-5k, and Nutrition-5k in tfrecord format. This is required for faster training.

You have done set up the datasets for **build_model.ipynb**. 🎉

### Issues

Please don't hestitate to raise any issues [here](https://github.com/Cheng-K/FoodNet/issues) if you encounter them during the installation steps.
