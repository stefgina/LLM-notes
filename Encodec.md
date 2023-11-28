# EnCodec: High Fidelity Neural Audio Compression


[High Fidelity Neural Audio Compression](https://arxiv.org/pdf/2210.13438.pdf)https://arxiv.org/abs/2210.13438 paper.

  
The "EnCodec" paper presents a state-of-the-art audio codec that leverages neural networks for real-time, high-fidelity audio compression. The key aspects of the EnCodec system are as follows:

1. **Encoder-Decoder Architecture**: The model is based on a streaming, convolutional-based encoder-decoder structure. It processes audio signals with sequential modeling components applied to the latent representation on both the encoder and decoder sides. This design is effective for various audio-related tasks such as source separation, enhancement, and neural vocoding​[](https://ar5iv.org/abs/2210.13438)​.
    
2. **Residual Vector Quantization (RVQ)**: RVQ is used to quantize the encoder's output. It works by projecting an input vector onto the closest entry in a codebook, then computing the residual after quantization, and further quantizing it using a second codebook. This process is iterated to refine the quantization​[](https://ar5iv.org/abs/2210.13438)​.
    
3. **Language Modeling and Entropy Coding**: A small Transformer-based language model is trained to compress the obtained representation further. This model aims to maintain faster than real-time end-to-end compression/decompression on a single CPU core​[](https://ar5iv.org/abs/2210.13438)​.
    
4. **Training Objective**: The training objective includes a reconstruction loss term, a perceptual loss term (via discriminators), and the RVQ commitment loss​[](https://ar5iv.org/abs/2210.13438#:~:text=We%20detail%20the%20training%20objective,and%20the%20RVQ%20commitment%20loss)​.
    
5. **Dataset and Training**: The model is trained on diverse audio domains, including speech, noisy speech, music, and general audio. It uses datasets like DNS Challenge, Common Voice, AudioSet, FSD50K, and Jamendo. The training strategy involves mixing different sources from these datasets​[](https://ar5iv.org/abs/2210.13438)​. Training is performed for 300 epochs with the Adam optimizer​[](https://ar5iv.org/abs/2210.13438#:~:text=We%20train%20all%20models%20for,each%2C%20a%20learning%20rate%20of)​.
    
6. **Technical Contributions and Evaluations**: The paper posits that designing end-to-end neural compression models involves intertwined choices, including the encoder-decoder architecture, quantization method, and perceptual loss. Extensive human evaluations (MUSHRA tests) were conducted to assess the codec's performance in various settings, including monophonic audio at 24 kHz and stereophonic audio at 48 kHz. Te EnCodec model demonstrated superior performance across all evaluated settings compared to baseline methods​[](https://ar5iv.org/abs/2210.13438)​.
![[imgs/encodec.png]]
