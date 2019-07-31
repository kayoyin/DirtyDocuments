# Scanned Document Denoiser

Implementation of a CNN ensemble model and CycleGAN for cleaning scanned documents, to faciliate OCR subsequently.

Inspired from denoising dirty documents Kaggle [challenge](https://www.kaggle.com/c/denoising-dirty-documents)

[Medium article](https://medium.com/illuin/cleaning-up-dirty-scanned-documents-with-deep-learning-2e8e6de6cfa6) detailing the task, solutions and results. 

## To use the ensemble model (CNN or XGB):
* Put dirty images in `data/x_train`, associated target clean images in `data/y_train`, dirty test images in `data/x_test`.
* Run `data_augmentation.ipynb`
* Run `base_learners.ipynb`
* Run `stacker_models.ipynb`

## To use the CycleGAN model:
* Put dirty images for training/testing in `gan_data/trainA` / `gan_data/testA` 
* Put clean images in  `gan_data/trainB` / `gan_data/testB` 
* The dirty and clean images do not need to be paired
* Run `CycleGAN.ipynb`
