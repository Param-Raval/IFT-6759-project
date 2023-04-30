# IFT-6759-project
## Project on SemEval 2022 Task 6 Intended Sarcasm Detection 

---

### Requirements

The code was created and executed on *Python 3.10.9* and the virtual environment can be created using `environment.yml` using

```
conda env create -f environment.yml
```

or using `requirements.txt` using

```
pip install requirements.txt
```

Generally, machine learning models were developed using `scitkit-learn`, LSTM models using `tensorflow 2.x` and Transformer-based models were loaded using `transformers` and fine-tuned using `PyTorch`.


Transformer-based models were trained on Colab GPU Basic.

---

### Project Structure

- `data` contains all the data used in this project. The augmented data for each of the two tasks can be found in their own respective subfolders. This folder is for representation purpose only since the files are expected to be in the same directory as the notebooks for them to run.
- `notebooks` contains 5 self-contained notebooks.
    - `SemEval_Task_6_Task_A_Machine_Learning_+_Aug.ipynb` contains the code to train various machine learning models on the Task A data. It also contains the code to generate mutation-based augmented datasets and experimental results on each model. It uses `mutate.py` and `synm.json` to generate and save mutations.
    - `SemEval_Task_6_Task_A_DL_BERT.ipynb` uses pretrained Transformer models from `transformers` and reports results after fine-tuning them on the original data or the augmented data.
    - `SemEval_Task_6_Task_A_Exploring.ipynb` tests various word vectorization techniques (Bow, Word2Vec, and TF-IDF) to finalise one method to use for the rest of the modeling methods. It also explores LSTM-based models.
    - `SemEval_Task_6_Task_B_Machine_Learning_+_Explore.ipynb` tests various Machine Learning models on the original task B data.
    - `SemEval_Task_6_Task_B_DL_with_Aug.ipynb` uses most of the models reported in Task A to fine-tune using the augmented task B dataset and report the experimental results.

---

### Run
The notebooks are self-contained (except for the ones that use augmented data). Each notebook can fetch the original data and run each of the model-wise segregated experiments.

For Task A, the augmentation code in `SemEval_Task_6_Task_A_Machine_Learning_+_Aug.ipynb` can generate and save the data found in `data/task-a-aug`. For Task B, the files in `data/task-b-aug` are necessary to run the Transformer-based models. The path can be modified as needed.

---

### Report
More details on the project, references, and methods can be found in the report.
