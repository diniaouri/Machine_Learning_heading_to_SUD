# Machine_Learning_heading_to_SUD
**Dimitra Niaouri, Bruno Machado Carneiro, Michele Linardi, Julien Longhi**

Repository of the paper: "Machine Learning is heading to the SUD (Socially Unacceptable Discourse) analysis: from Shallow Learning to Large Language Models to the rescue, where do we stand?" 

## Data

Details on the data acquisition and preprocessing are described [here](data/data.md).


## Dependencies  

* **Install all the dependencies:**  
```
python3 -m pip install -r requirements.txt
```
## Repository Structure
```
Machine_Learning_heading_to_SUD
├── data
    │   ├── concatenate.py
    │   ├── generate_dataset.py
    │   └── preprocessing.py
└── src
    ├── CLMs
    │   ├── Llama2.py
    │   ├── Mistral.py
    │   └── MPT.py
    ├── MLMs
    │   ├── BERT_models.py
    │   ├── BERT_tf_hub.json
    │   ├── load_data.py
    │   ├── test.py
    │   └── train.py
    └── SLMs
        ├── GB.py
        ├── LR.py
        ├── MNB.py
        ├── RF.py
        └── SVM.py
```

## Usage  

### *For CLMs*
* **Arguments:**
```
--data          Path to the dataset
```

### *For MLMs*

### Training  

```
train.py [--data data_path] 
         [--mode {binary, multi-class}]
         [--batch_size batch_size]
         [--epochs epochs_count]
         [--lr learning_rate]
         [--smoothing smoothing_rate]
```

* **Arguments:**
```
--data          Path to the dataset
--mode          Perform binary or multi-class SUD classification
--batch_size    Batch size
--epochs        Number of epochs
--lr            Learning rate
--smoothing     Label smoothing rate
```

### Testing  

```
test.py [--data data_path] 
        [--model model_path]
        [--mode {binary, multi-class}]
```

* **Arguments:**
```
--data          Path to the dataset
--model         Path to the trained model
--mode          Perform binary or multi-class SUD classification
```

### *For SLMs*
* **Arguments:**
```
--data          Path to the dataset
```
      
