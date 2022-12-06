# Salience-Biased-Reduced-Focal-Loss-CV703-final-project

This project has been done as a final project for CV703 - Visual Object Recognition and Detection at MBZUAI. The project is about proposing a Salience Biased Reduced Focal Loss (SBRF) which helps in increasing the contributions of well-classified samples to overcome the issue of class imbalanced in aerial images datasets. Our work is based on:

1. Detectron2.
2. REDUCED FOCAL LOSS: 1st PLACE SOLUTION TO XVIEW OBJECT DETECTION IN SATELLITE IMAGERY (https://arxiv.org/pdf/1903.01347.pdf).
3. Salience Biased Loss for Object Detection in Aerial Images (https://arxiv.org/pdf/1810.08103.pdf).

### Detectron2
Follow instructios to install Detectron2 from (https://detectron2.readthedocs.io/en/latest/tutorials/install.html)

### Dataset
Download [iSAID from](https://captain-whu.github.io/iSAID/dataset.html)

### Training 
Our modifications were on these files in the Detectron2 directory. Follow these steps to start tranining:

1. Generate Saliency map : sal_map/Generating_sal_maps.ipynb
2. Add loss function: detectron2/detectron2/modeling/proposal_generator/reduced_focal_loss.py
3. Replace the RPN script with our file: detectron2/detectron2/modeling/proposal_generator/rpn.py
4. Replace (class SimpleTrainer(TrainerBase)) with our in detectron2/detectron2/engine/train_loop.py
