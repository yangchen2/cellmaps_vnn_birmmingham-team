# Visible Neural Networks (VNN) for Drug Response Prediction

This repository focuses on optimizing a **Visible Neural Network (VNN)** model to predict drug responses.  
The work builds on the [cellmaps_vnn](https://github.com/idekerlab/cellmaps_vnn) framework and leverages resources from [nest_vnn](https://github.com/idekerlab/nest_vnn).

---

## 🚀 Goal
To optimize hyperparameters of a VNN model and evaluate performance for drug response prediction.

---

## ⚙️ Methodology
- **Hyperparameter optimization**  
  Adjusted parameters in `config.yml`, including:
  - Epochs  
  - Learning rate  
  - Weight decay  
- **Model evaluation**  
  Compared generated predictions with ground truth.  
  Performance metrics:
  - Mean Squared Error (MSE)  
  - Root Mean Squared Error (RMSE)  

---

## 🖥️ Environment Setup
- **Platform**: TACC (Texas Advanced Computing Center)  
- **Environment**: `vnn_env`  
- **Reference**: [TACC Setup Guide](https://training.cm4ai.org/courses/7/pages/tacc-environment-setup)  

---

## 📚 Training and Prediction

### Training
Run on TACC idev node in `vnn_env` environment:
```bash
cellmaps_vnncmd.py train ./outdir_training \
    --inputdir examples \
    --config_file examples/config.yaml
```

### Prediction
```bash
cellmaps_vnncmd.py predict ./outdir_prediction2 \
    --inputdir ./outdir_training2 \
    --config_file examples/config.yaml
```

---

## 🎨 Visualization
Network annotations can be visualized in **NDEx**:
```bash
cellmaps_vnncmd.py annotate annotate1 \
    --model_predictions outdir_prediction6/ \
    --ndexuser <your_email> \
    --ndexpassword <your_password> \
    --parent_network 0b7b8aee-332f-11ef-9621-005056ae23aa \
    --visibility
```

---

## 🔮 Future Directions
- Automate scripts and batch submission for **full-factorial hyperparameter optimization**.  
- Evaluate performance across multiple datasets.  
- Develop more robust AI/ML/DL models for training and predictions.  

---

## 📖 References
- [cellmaps_vnn](https://github.com/idekerlab/cellmaps_vnn)  
- [nest_vnn](https://github.com/idekerlab/nest_vnn)  
- [TACC Environment Setup](https://training.cm4ai.org/courses/7/pages/tacc-environment-setup)  
