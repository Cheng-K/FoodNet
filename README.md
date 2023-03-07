<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Cheng-K/FoodNet">
    <img src="images/FoodNet.svg" alt="Logo">
  </a>

  <h1></h1>
  <p align="center">
    Food Ingredients Recognition and Calorie Estimation using Multi-Task Deep Learning
    <br />
    <br />
    <a href="https://github.com/Cheng-K/FoodNet-App">View Demo</a>
    ·
    <a href="https://github.com/Cheng-K/FoodNet/issues">Report Bug</a>
    ·
    <a href="https://github.com/Cheng-K/FoodNet/issues">Request Feature</a>
  </p>
</div>
<br/>
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

This is my final year project for my undergraduate course. This project aims to propose a multi-task deep learning model that detects the category and
ingredients of a captured food image and estimates the food calories and macronutrients consumed
by users.

This project is made up of two repositories : this & [FoodNet-App](https://github.com/Cheng-K/FoodNet-App). This repository showcase the development of the deep learning model used in the project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

- [![Keras][keras]][keras-url]
- [![Tensorflow][tensorflow]][tensorflow-url]
- [![Pandas][pandas]][pandas-url]
- [![Python][python]][python-url]
- [![Anaconda][anaconda]][anaconda-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

- [Anaconda Distribution](https://docs.anaconda.com/anaconda/install/index.html)

### Installation

1. Open Anaconda Prompt
2. Clone the repo
   ```
   git clone https://github.com/Cheng-K/FoodNet.git
   ```
3. Change to project root directory
   ```
   cd FoodNet
   ```
4. Create new environment with environment.yml
   ```
   conda env create -f environment.yml
   ```
5. Activate the environment
   ```
   conda activate PY38-TF28
   ```
6. Navigate to _Food Datasets_ subdirectory and follow the instructions from each READMEs in each further subdirectory to set up the required datasets.

7. _(Optional)_ Set up GPU by installing [CUDA Toolkit 11.2](https://developer.nvidia.com/cuda-toolkit-archive) and [cuDNN SDK 8.1.0](https://developer.nvidia.com/cudnn) or follow [the TensorFlow guide](https://www.tensorflow.org/install/pip).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Usage

To effectively use this repository, the following shows the functionality of each directory and files.

Directory : **Food Datasets**

- Contains folders that store different types of dataset used in this project.
- A README is provided in each directory with attached sources and instructions to obtain and set up the dataset.
- Each folder also have a script that preprocess the stored dataset.
- The final-dataset stores the preprocessed dataset that is used for training the model
  after running all the preprocessing scripts for each dataset

Directory : **Ingredient Embeddings**

| File                                   | Description                                                                                                                                                          |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ingredient_embeddings_similarity.ipynb | Generates text embeddings to compare ingredients similarity so the missing nutritional information of an ingredient can be imputed with the most similar ingredient in the nutritional database. |

Directory : **main**

| File                | Description                                                                                                                                                                                           |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| build_model.ipynb   | Main file that contains code to build and train the proposed deep learning models                                                                                                                     |
| data_pipeline.ipynb | Prerequisite file for running _build_model.ipynb_. It serialize all the datasets into tfrecord files so that efficient data pipeline can be constructed to feed the data into the deep learning model |

<br></br>
In summary, the installation steps should set up everything including the datasets. All there is left is executing the **build_model.ipynb** to train the proposed deep learning model.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Cheng Kei Ong - chengkei.ong@outlook.com
<br/>
<br/>
[![LinkedIn][linkedin-shield]][linkedin-url]

Project Link: [https://github.com/Cheng-K/FoodNet](https://github.com/Cheng-K/FoodNet)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

- [Nutrition5k](https://github.com/google-research-datasets/Nutrition5k)
- [Recipes5k](http://www.ub.edu/cvub/recipes5k/)
- [Food101](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/)
- [FoodData Central](https://fdc.nal.usda.gov/index.html)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[linkedin-shield]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url]: https://www.linkedin.com/in/chengkei-ong
[product-screenshot]: images/screenshot.png
[keras]: https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white
[keras-url]: https://keras.io/
[tensorflow]: https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white
[tensorflow-url]: https://www.tensorflow.org/
[pandas]: https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white
[pandas-url]: https://pandas.pydata.org/
[python]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[python-url]: https://www.python.org/
[anaconda]: https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white
[anaconda-url]: https://www.anaconda.com/
[kaggle]: https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white
[kaggle-url]: https://www.kaggle.com/
