## Encoders Decoders
- Sequence to Sequence( seq2seq): eg. RNN enc/dec, for short sentence translation


## Auto-Encoders
You just compare the Encoder input and the Decoder output (Reconstruction Loss)
- Anomaly Detection: For Loss you compare the input with the output, If for a test sample the loss is high (while the auto-encoder is trained on 'healthy' samples) then you have an anomaly.
- SuperResolution: image + noise -> image
- Dimensionality Reduction (eg. Image Compression): you just take the encoder, and compress
- Feature Extraction: The encoding part (feat. extract) + Classifers/Regressors etc.


![](ae.png)

## Variational Auto-Encoders

![](imgs/vae.png)


## Attention 



## Transformers