**English** | [简体中文](README.zh-CN.md)

# Paired Fundus Disease Recognition

Notebook experiments for multilabel recognition from paired left/right fundus photographs, using ODIR data, a shared ResNet18d backbone, paired-eye feature fusion, focal loss, and model evaluation.

**Category:** Artificial Intelligence · Computer Vision  
**Stack:** Python · PyTorch · PyTorch Lightning · timm · OpenCV · Jupyter

## Repository contents

| Material | Purpose |
| --- | --- |
| [DSrenew.ipynb](DSrenew.ipynb) | Paired-image loading, augmentation, ResNet18d modeling, training, and evaluation |
| [multi label.ipynb](multi%20label.ipynb), [main.ipynb](main.ipynb) | Additional experiment variants |
| `*-checkpoint.ipynb` | Saved notebook copies |
| `*.docx`, `*.pptx` | Chinese design documentation and competition presentation |

The documents describe a broader web system for patient management, visualization, and an AI assistant. That application's frontend, backend, and database are not included; the runnable material here is the notebook code.

## Prepare data

The notebooks reference paired ODIR images, training spreadsheets, and CSV files such as `ODIR-5K_Training_Annotations(Updated)_V2.xlsx` and `XYZ_ODIR.csv`. Update paths and schemas to match authorized local data.

The original [dataset sharing link](https://pan.baidu.com/s/1ocOTqy6AFXXo6iVviKA-Bg?pwd=2023), code `2023`, is retained for reference. Availability and dataset rights are separate from the code license. Check label order, patient-level splitting, and preprocessing before training.

## Environment and use

No pinned dependency manifest is included. In an isolated environment, install a compatible PyTorch/torchvision pair for your hardware, then prepare the notebook dependencies:

```bash
python -m pip install jupyter pandas openpyxl numpy scikit-learn matplotlib pillow opencv-python pytorch-lightning timm torchmetrics albumentations
jupyter notebook
```

Open `DSrenew.ipynb`, inspect the cells, configure local files, and run the experiment sections in order. Older library APIs and explicit CUDA calls may require dependency or device adjustments. This is a starting dependency list, not a tested lockfile.

## Limitations

This repository documents experiments rather than a clinically validated diagnostic product. Figures in the original Chinese materials are not independently reproduced here. No clinical effectiveness or complete deployed web application is claimed. Reproduction requires data access, compatible dependencies, compute resources, and a fresh evaluation.

## Author and license

Author / maintainer: [https://github.com/OOOHGOD](https://github.com/OOOHGOD).

Eligible original contributions are under the [MIT License](LICENSE), permitting commercial use and modification with preservation of copyright and license notices in copies or substantial portions. [License scope](LICENSE_SCOPE.md) explains third-party exclusions and upstream terms.
