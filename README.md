# Interactive Reconstruction of Monte Carlo Image Sequences using a Recurrent Denoising Autoencoder
Tensorflow Implementation and some visual results of SIGGRAPH'17 paper: [Interactive Reconstruction of Monte Carlo Image Sequences using a Recurrent Denoising Autoencoder](https://research.nvidia.com/sites/default/files/publications/dnn_denoise_author.pdf) by Chakravarty R. Alla Chaitanya, Anton Kaplanyan, Christoph Schied, Marco Salvi, Aaron Lefohn, Derek Nowrouzezahrai and Timo Aila

## Architecture
We use the same architecture proposed in the paper instead we change the recurrent block to [ConvLSTM](https://arxiv.org/pdf/1506.04214.pdf) blocks.

## Data Acquisition
We use [pbrt-v3](https://www.pbrt.org/fileformat-v3.html) to render 1 spp, 4096 spp, and auxiliary features as training pairs. Example input features in grey scale and reference in bathroom scene (a) 1 spp MC rendering with Halton sampler, (b) depth, (c) shading normal x-axis, (d) shading normal y-axis, (e) roughness, and (f) 4096 spp reference.

![training data](https://github.com/yuyingyeh/rdae/blob/master/fig_features.png)

Example of our training sequence:
![training sequence](https://github.com/yuyingyeh/rdae/blob/master/fig_sequence.png)

## Visual Results
Right: Noisy 1 spp input RGB sequence

Middle: Reconstructed sequence

Left: Reference 4096 spp sequence

![video1](https://github.com/yuyingyeh/rdae/blob/master/m4outVideo.gif "video1")

![video2](https://github.com/yuyingyeh/rdae/blob/master/m4outVideo2.gif "video2")
