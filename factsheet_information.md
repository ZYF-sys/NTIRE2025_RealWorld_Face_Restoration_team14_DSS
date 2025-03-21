## FactSheet

We use a fine-tuned DiffBIR(https://github.com/XPixelGroup/DiffBIR) for the initial restoration in the first stage, then apply StableSR(https://github.com/IceClear/StableSR) to align with real-world facial features, and finally use SUPIR(https://github.com/Fanghua-Yu/SUPIR) to enhance facial details.

Specifically, DiffBIR was trained on ImageNet-1k with CodeFormer degradation and filtered laion2b-en. StableSR was trained on DIV2K，DIV8K and OutdoorSceneTraining datasets. SUPIR's training data includes 20 million high-quality images with text descriptions, 70K face images and 100K negative-quality. For detailed training hyperparameters, please refer to the corresponding paper. 

We fine-tune the SwinIR component of DiffBIR using the FFHQ dataset. The related training hyperparameters can be found in the following configuration files:
`models/team14_DSS/DiffBIR/configs/train/train_stage1.yaml`



