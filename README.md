# Assignment 9 — Image Classification using CNN (Cats vs Dogs)

## Objective
Develop a Convolutional Neural Network (CNN) that automatically classifies pet images into
**Cats** and **Dogs**, to help an animal welfare organization automate image sorting.

## Dataset Link
[Cats vs Dogs Dataset — Kaggle](https://www.kaggle.com/datasets/bhavikjikadara/dog-and-cat-classification-dataset)

> The dataset is **not** included in this repository. Download it from the Kaggle link above,
> or use the Kaggle API as shown in the notebook.

## Libraries Used
- `tensorflow` / `keras` — model building, training, `ImageDataGenerator`
- `numpy` — numerical operations
- `matplotlib`, `seaborn` — plotting (sample images, accuracy/loss curves, confusion matrix)
- `scikit-learn` — precision, recall, F1-score, confusion matrix, classification report
- `Pillow (PIL)` — image loading/inspection
- `pathlib`, `os`, `glob` — file system / folder structure inspection

## Methodology
1. **Data Understanding:** Loaded the dataset, inspected the folder structure, counted images
   per class, checked image dimensions, and visualized five sample images with labels.
2. **Data Preprocessing:** Resized all images to 128×128, normalized pixel values to [0, 1] via
   rescaling, and split the data into 80% training / 20% testing using Keras'
   `ImageDataGenerator(validation_split=0.2)` and `flow_from_directory`.
3. **Model Development:** Built a CNN (architecture below), compiled with the Adam optimizer,
   binary crossentropy loss, and accuracy metric, then trained for 10 epochs.
4. **Model Evaluation:** Evaluated test accuracy, precision, recall, and F1-score; plotted a
   confusion matrix, and accuracy/loss vs. epoch curves.
5. **Conclusion:** Summarized findings, the role of convolution/pooling layers, a CNN advantage
   over ANN, and a CNN limitation.

## CNN Architecture
| Layer | Details |
|---|---|
| Conv2D | 32 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 64 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 128 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Flatten | — |
| Dense | 128 neurons, ReLU |
| Dense (Output) | 1 neuron, Sigmoid |

- **Optimizer:** Adam
- **Loss:** Binary Crossentropy
- **Metric:** Accuracy
- **Epochs:** 10

## Results
*(Fill in after running `Assignment-9.ipynb` in your own environment — e.g. Google Colab or
Kaggle Notebooks with GPU — since results depend on the actual training run.)*

| Metric | Value |
|---|---|
| Test Accuracy | `TODO` |
| Precision | `TODO` |
| Recall | `TODO` |
| F1-Score | `TODO` |

Include your Accuracy vs Epoch graph, Loss vs Epoch graph, and Confusion Matrix images here
(export them from the notebook and add to an `images/` folder, then embed with
`![Confusion Matrix](images/confusion_matrix.png)`).

**Observations:**
1. `TODO`
2. `TODO`
3. `TODO`
4. `TODO`

## Conclusion
`TODO` — write a 100–150 word conclusion covering key findings, the importance of convolution
and pooling layers, one advantage of CNN over ANN for image classification, and one limitation
of CNN. (A draft template is provided at the end of `Assignment-9.ipynb` — personalize it with
your actual results before submitting.)

## How to Run
1. Open `Assignment-9.ipynb` in Google Colab or Kaggle Notebooks (GPU runtime recommended).
2. Download the dataset (via Kaggle API or manual upload) so it matches the `DATASET_DIR`
   path used in the notebook.
3. Run all cells top to bottom.
