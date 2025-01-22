# Evaluating Image Fusion Techniques for Low Light Surveillance

This repository contains the code and results for the paper **"Evaluating Image Fusion Techniques for Improved Low Light Surveillance"** published in the *International Journal of Engineering Research in Computer Science and Engineering (IJERCSE)*, June 2024. The research conducts a comparative analysis of state-of-the-art deep learning-based image fusion models to enhance low-light surveillance.

## Repository Contents

### Implemented Models:
1. **DIDFuse** - Autoencoder-based image fusion method for low-light scenarios.
 <img width="735" alt="Screenshot 2025-01-22 at 3 03 30 PM" src="https://github.com/user-attachments/assets/34017f64-5948-4416-9334-1244fd8ea92c" />
 
2. **SwinFuse** - Transformer-based image fusion using Swin Transformer for attention-guided cross-domain feature fusion.
<img width="907" alt="Screenshot 2025-01-22 at 3 03 56 PM" src="https://github.com/user-attachments/assets/290284b3-c4dd-4c70-a0cb-99f644f90d86" />

3. **Dual-Branch Network** - Infrared and visible image fusion leveraging dense convolutional blocks.
<img width="933" alt="Screenshot 2025-01-22 at 3 04 22 PM" src="https://github.com/user-attachments/assets/71ca0a9e-13c3-4b2e-85c3-f1dd6538e746" />

4. **DenseFuse** - Dense block-based convolutional neural network for comprehensive feature extraction and fusion.
<img width="796" alt="Screenshot 2025-01-22 at 3 04 41 PM" src="https://github.com/user-attachments/assets/98e15f7a-ac6b-47c7-a6ba-9a554ea1a4a6" />

### Dataset:
- **LLVIP Dataset**: This dataset includes paired visible and infrared images under low-light conditions. It contains 16,836 image pairs across 26 diverse scenes captured between 1800 and 2200 hours.
- **Preprocessing**: Images are converted to grayscale and resized to 256x256 for uniformity during training.
  <img width="474" alt="Screenshot 2025-01-22 at 3 02 16 PM" src="https://github.com/user-attachments/assets/c539e861-a167-433b-86dd-230855c10e45" />


### Results:
- Quantitative analysis using metrics like Entropy (EN), Mutual Information (MI), Peak Signal-to-Noise Ratio (PSNR), Visual Information Fidelity (VIF), and more.
- Qualitative results showcasing fused images from each method.
<img width="737" alt="Screenshot 2025-01-22 at 3 02 39 PM" src="https://github.com/user-attachments/assets/f43b046a-fb82-4c73-b60b-5f5a75e00b86" />

### Dependencies:
- Python >= 3.8
- PyTorch >= 1.9
- NumPy, Matplotlib, OpenCV, SimpleITK
- Other requirements are listed in `requirements.txt`.

## Usage

### Data Preparation
- Download the [LLVIP Dataset](#) and place it in the `datasets/LLVIP` folder.

### Training Models
Run the training script with the desired model:
```bash
python scripts/train.py --model <model_name> --dataset datasets/LLVIP
```

### Evaluation
Evaluate the trained models using:
```bash
python scripts/evaluate.py --model <model_name> --dataset datasets/LLVIP
```

### Results Visualization
Fused images and metrics are saved in the `results/` folder.

## Citation
If you use this code or dataset, please cite the paper:
```
@article{(IJERCSE Volume 11 Issue 6 June 2024,
  title={Evaluating Image Fusion Techniques for Improved Low Light Surveillance},
  author={Mishra, Akshat and Yadav, Dipesh Kumar and Bathija, Nikhil},
  journal={IJERCSE},
  volume={11},
  number={6},
  pages={150--154},
  year={2024}
}
```

## License
This project is licensed under the MIT License.
