# Chicken Coccidiosis Classification

This project aims to classify chicken fecal samples into two categories: diseased (Coccidiosis) and healthy. The classification is based on analyzing images of the fecal samples using computer vision techniques.

## Project Structure

The project follows a modular structure, consisting of several stages and pipelines which includes :-

1. `stage_01_data_ingestion.py`: This stage is responsible for data ingestion. It includes functions for downloading, extracting, and preprocessing the dataset.
2. `stage_02_prepare_base_model.py`: In this stage, the base model for the classification task is prepared. It involves loading a pre-trained model, modifying it if necessary, and preparing it for training.
3. `stage_03_training.py`: The training stage is responsible for training the model using the prepared dataset. It includes functions for data augmentation, model training, and saving the trained model.
4. `stage_04_evaluation.py`: This stage focuses on evaluating the performance of the trained model. It includes functions for loading the trained model, performing inference on test data, and calculating evaluation metrics.

## Dependencies

To run this project, you need the following dependencies:

- Python (version 3.8 or above)
- TensorFlow 
- Flask 
- DVC 

Make sure you have installed the required dependencies before running the project.


## Workflows
* Update config.yaml
* Update secrets.yaml [Optional]
* Update params.yaml
* Update the entity
* Update the configuration manager in src config
* Update the components
* Update the pipeline
* Update the main.py
* Update the dvc.yaml

## Usage

1. Clone the repository:

```bash
git clone https://github.com/Pratik94229/Chicken-Disease-Classification-Project

```
```
cd Chicken-Disease-Classification-Project
```

2. Create a conda environment after opening the repository
```
conda create -p venv python==3.8 
conda activate venv/

```

3. Install the dependencies:

```bash
pip install -r requirements.txt
```


4. Finally run the following command

```
python app.py

```

5. Open Terminal

### DVC cmd
```
dvc init
dvc repro

```
6. For visualizing pipeline
```
dvc dag

```

7. Flask App:

To create a front-end interface for the application, run the Flask app:

```bash
python app.py
```

8. Access the app:

Open your browser and go to `http://localhost:5000` to access the application.

## Conclusion

This project demonstrates the classification of chicken fecal samples as diseased or healthy using computer vision techniques. The modular structure and the use of pipelines make it easy to follow and reproduce the workflow. The Flask app provides a user-friendly interface for interacting with the classification model.

For more details, refer to the individual implementation files and comments within the code.
