# CLIP-SAFMOE

**Semantic-Adaptive Fusion with Mixture-of-Emotion-Experts for Facial Expression Recognition**

CLIP-SAFMOE is an experimental deep-learning project for seven-class facial expression recognition using the RAF-DB dataset. The accompanying notebook contains the model implementation, training workflow, and evaluation outputs.

## Results

The H100 experiment notebook is named `CLIP_SAFMOE_RAFDB_H100_92.41.ipynb`.

The reported results should be interpreted according to the evaluation procedure and data split used in the notebook. Verify the evaluation cells before presenting any metric as official test-set performance.

## Architecture

The project explores the following components:

- **Adaptive Scale Fusion (ASF):** Combines visual features from multiple Vision Transformer layers.
- **Semantic Alignment Module (SAM):** Uses CLIP text representations to provide emotion-related semantic conditioning.
- **Mixture-of-Emotion-Experts (MoEE):** Uses multiple expert networks with routed computation.
- **CLIP ViT-L/14 backbone:** Provides pretrained visual representations.
- **LoRA adapters:** Support parameter-efficient adaptation.
- **Test-time augmentation (TTA):** Evaluates predictions across augmented image views.

Refer to the notebook for the exact implementation and configuration of each component.

## Dataset

The project uses **RAF-DB (Real-world Affective Faces Database)** for seven basic facial-expression classes:

- Surprise
- Fear
- Disgust
- Happiness
- Sadness
- Anger
- Neutral

The dataset is not included in this repository. Obtain it through an authorized distribution channel and follow its access terms.

## Repository Contents

```text
CLIP-SAFMOE/
├── README.md
└── CLIP_SAFMOE_RAFDB_H100_92.41.ipynb
```

## Running the Notebook

1. Open the notebook in Jupyter, Google Colab, or Kaggle.
2. Select a compatible GPU runtime. The recorded experiment uses an NVIDIA H100.
3. Obtain authorized access to RAF-DB and make the dataset available in the runtime.
4. Check and update dataset paths and output directories for your environment.
5. Install any missing dependencies as indicated by the notebook.
6. Run the cells in order to execute the workflow and inspect the evaluation outputs.

Exact reproduction may depend on the dataset split, preprocessing, pretrained weights, software environment, and hardware. Environment-specific paths may need to be updated.

## Reproducibility

The notebook includes code and saved outputs for the recorded experiment. Saved outputs are evidence of that notebook run, but results can vary with changes to data, configuration, dependencies, and runtime.

## Disclaimer

This repository is an experimental research implementation. Reported performance applies to the specific configuration and evaluation procedure used; it is not a guarantee of performance on other datasets or in real-world deployment.
