# A Patch-based Method for Underwater Image Enhancement with Denoising Diffusion Models
Binglei Bao, Haisheng Xia, Fei Liao, Jintao Chen, Binglu Wang, Zhijun Li

*This repository introduces the paper: "A Patch-based Method for Underwater Image Enhancement with Denoising Diffusion Models", and includes enhancement results from various public datasets and real-world scene images.*

Abstract: *The enhancement of underwater images has emerged as a significant technological challenge in advancing marine research and exploration tasks. Due to the scattering of suspended particles and absorption of light in underwater environments, underwater images tend to present blurriness and predominantly color distortion. In this study, we propose a novel approach utilizing denoising diffusion models to improve underwater degraded images. After training the noise estimation network of the denoising diffusion models, we accelerate the deterministic sampling process with denoising diffusion implicit models. We also propose a patch-based method by implementing average sampling between overlapping image patches at each sampling step, enabling the generation of images at arbitrary resolution while preserving their natural appearance and details. Through benchmark experiments, we illustrate that our method outperforms or closely approaches state-of-the-art techniques in terms of effectiveness and performance. We demonstrate that our approach reduces the interference of underwater environments with the semantic information of the images by salient object detection experiments.*

## Method
![method](Fig/method.png)
Our patch-based method for UIE with denoising diffusion models. (a) Overview of the forward process and the reverse process of conditional diffusion models. (b) Example of patch segmentation for underwater degraded images $\tilde{\mathbf{x}}$ when the stride of the sliding window is equal to the patch size (in this case, the patches are non-overlapping except for the margin regions). (c) The whole execution process of our methods. We segment both the conditional image $\tilde{\mathbf{x}}$ and each generated image $\mathbf{x}_{1...T}$ at each step into patches. The overlapping patches noise $\bm{\epsilon}_{\theta}$ is merged by mean after the noise estimation network.

## Result
### [RUIE](https://github.com/dlut-dimt/Realworld-Underwater-Image-Enhancement-RUIE-Benchmark)
![img1](static_cmp/2687.jpg)
![img1](static_cmp/3192.jpg)
![img1](static_cmp/3408.jpg)
![img1](static_cmp/A_224.jpg)
![img1](static_cmp/B_260.jpg)
![img1](static_cmp/bg_72.jpg)
![img1](static_cmp/bg_93.jpg)
![img1](static_cmp/blue_86.jpg)
![img1](static_cmp/green_25.jpg)

### [UIEB](https://li-chongyi.github.io/proj_benchmark.html)
![img1](Fig/UIEB/merged_153_img_.png)
![img1](Fig/UIEB/merged_57_img_.png)
![img1](Fig/UIEB/merged_200_img_.png)
### [EUVP](https://irvlab.cs.umn.edu/resources/euvp-dataset)
![img1](Fig/EUVP/merged_264294_00027762.jpg)
![img1](Fig/EUVP/merged_264477_n02655020_4025.JPEG)
![img1](Fig/EUVP/merged_264839_00027594.jpg)
### The Real-world Camera Captures Images
#### Artificial Underwater Scenes
![img1](Fig/Artificial/merged_frame_00002.png)
![img1](Fig/Artificial/merged_frame_00015.png)
#### Lake AUV Capture

## GIF

![gif1](gif/19_img_.gif)
![gif2](gif/233_img_.gif)
![gif3](gif/3408.gif)
![gif4](gif/bg_72.gif)
![gif5](gif/blue_86.gif)

## Preview under different parameters
![gif6](gif/final_image_new.gif)
