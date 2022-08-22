# rnnoise_no-band-below-1k_envelope-filter


# References:

Paper: [A Hybrid DSP/Deep Learning Approach to Real-Time Full-Band Speech Enhancement](https://jmvalin.ca/papers/rnnoise_mmsp2018.pdf)  

Rnnoise Github Repo: [RNNoise](https://github.com/xiph/rnnoise)

Percepnet Github Repo: [Percepnet-Keras](https://github.com/cookcodes/Percepnet-Keras)


# Revised point
The code is from [RNNoise](https://github.com/xiph/rnnoise).  
Revised points is as below:

1. use original frequency bin without bands below 1k frequency
2. use envelope filter (post filter) from percepnet
3. keep low energy noise (post-processing) for avoid unstable noise (human hearing feeling)


# usage


To compile, just type:




./autogen.sh  
./configure  
make





Optionally:


make install


While it is meant to be used as a library, a simple command-line tool is
provided as an example. It operates on RAW 16-bit (machine endian) mono
PCM files sampled at 48 kHz. It can be used as:


./examples/rnnoise_demo noisy_speech.raw output_denoised.raw


The output is also a 16-bit raw PCM file.
