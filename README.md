# MMDF: Mobile Microscopy Deep Framework
The aim of our project is to apply deep learning techniques in the field of optical imaging to images taken from mobile microscope. We consider data that consists of z-stack images of specimen (more details in dataset description). In this work we would like to use the next techniques:

- In-focus/out-of-focus images classification. When automatically scanning specimen, it is necessary to choose only in-focus images. In comparison to classical focus measure operators DL techniques allow not to lose small focused parts of the image.
- Fast scanning image deblurring. Obtaining of the high quality images requires much more time while scanning. The idea is to reuse DL deblurring techniques for fast scanning when we can reconstruct original image from one obtained from fast movement.
- Focus-stacking (Multi-Focus fusion). Because of the main feature of optical microscopes is shallow depth of focus, therefore volume specimen can not be studied from one focal length -- user should change it mechanically to understand the structure of sample. The idea is to apply all-in-focus technique to construct the image where all the parts are sharp.

![2018, Pfeil et al
“Mobile Microscopy and Automated Image Analysis”
](https://github.com/anastasiia-kornilova/MMDF/blob/master/pics/mobile_microscopy.PNG)

The code was written by:

- Egor Sevriugov and Kirill Shcherbakov - Focus stacking for volume specimens 
- Maria Begicheva and Olga Novitskaya - Deblurring and denoising
- Mikhail Salnikov and Anastasiia Kornilova - In-focus/out-of-focus images filtering

**MMDF: [Project](https://github.com/anastasiia-kornilova/MMDF) | [Report](https://drive.google.com/open?id=1CqEa_3949RtZsEntnwdQAmwvu4_Pf9zw) | [Presentation](https://docs.google.com/presentation/d/1Zyz_S27k98Ua2PimrDjv175B2vsp_7Ahts_au6_EAq8/edit#slide=id.g8634b66c95_0_101) | [Video report](https://youtu.be/6Lk_OicMbI0)**

**Multi-focus image fusion**
![](https://github.com/anastasiia-kornilova/MMDF/blob/master/pics/zoom_comparison.png)

**In/Out focus classificator**
![](https://github.com/anastasiia-kornilova/MMDF/blob/master/pics/in_out_focus_classificator.PNG)

**Image deblurring**
![](https://github.com/anastasiia-kornilova/MMDF/blob/master/pics/deblur.PNG)

## Prerequisites
- Python 3
- Google Colaboratory service
- PyTorch 1.4.0, Tensorflow 2.1.0, Keras 2.3.0

## Datasets info
The dataset contains the videos of z-stack scanning recorded by a smartphone microscope (150 specimen). Every scan is presented in 4 videos with different speed of scanning.


## Related Projects

- "DeblurGAN: Blind Motion Deblurring Using Conditional Adversarial Networks":
 [Paper](https://arxiv.org/pdf/1711.07064.pdf) | [Code](https://github.com/KupynOrest/DeblurGAN)
- "IFCNN: A General Image Fusion Framework Based on Convolutional Neural Network, Information Fusion, 54 (2020) 99-118":  [Paper](https://www.sciencedirect.com/science/article/abs/pii/S1566253518305505) | [Code](https://github.com/uzeful/IFCNN)
- "FFusionCGAN: An end-to-end fusion method for few-focus images using conditional GAN in cytopathological digital slides":  [Paper](https://arxiv.org/abs/2001.00692) | [Code](https://github.com/GengXieBo/fusion)
- "Assessing microscope image focus quality with deep learning. BMC Bioinformatics 19, 77 (2018)." [Paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-018-2087-4) | [Code](https://github.com/google/microscopeimagequality)
