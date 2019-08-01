# Scanned Document Denoiser

Implementation of an ensemble model with CNN autoencoder and image processing as base learners, and CNN or XGB meta learner, and CycleGAN for cleaning scanned documents, to faciliate OCR subsequently.

Inspired from denoising dirty documents Kaggle [challenge](https://www.kaggle.com/c/denoising-dirty-documents)

[Medium article](https://medium.com/illuin/cleaning-up-dirty-scanned-documents-with-deep-learning-2e8e6de6cfa6) detailing the task, solutions and results. 

## Dependencies

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

## References
* [Denoising Dirty Documents](https://www.kaggle.com/c/denoising-dirty-documents/overview) on Kaggle
* [Image Processing in OpenCV](https://docs.opencv.org/2.4/doc/tutorials/imgproc/table_of_content_imgproc/table_of_content_imgproc.html)
* [Image Processing + Machine Learning in R: Denoising Dirty Documents Tutorial Series](http://blog.kaggle.com/2015/12/04/image-processing-machine-learning-in-r-denoising-dirty-documents-tutorial-series/) by Colin Priest
* [Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://arxiv.org/pdf/1703.10593.pdf), by Zhu et al.
* [Keras Implementation](https://github.com/eriklindernoren/Keras-GAN/tree/master/cyclegan)of CycleGAN
