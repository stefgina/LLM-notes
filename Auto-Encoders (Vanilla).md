## Auto-Encoders {Unsupervised}
![](imgs/ae.png)

The idea is to compare the Encoder input and the Decoder output and minimise their difference.

- Anomaly Detection: For Loss you compare the input with the output, If for a test sample the loss is high (while the auto-encoder is trained on 'healthy' samples) then you have an anomaly.

- SuperResolution: image + noise -> image (*for loss you just compare the {image,image} without noise*)

- Dimensionality Reduction (eg. Image Compression): you are just utilising the trained encoder, to compress, for decompression use the decoder. (* try to push the latent vector low*)

- Feature Extraction: The encoding part (feat. extract) + Classifiers/Regressors etc. (*this is particularly useful when you have a lot of unlabelled data, and wanna build a classifier with just a few labelled data. Auto-Encoders are unsupervised.*)




## Variational Auto-Encoders {Unsupervised}
![](imgs/vae.png)
- Image Generation: VAEs can generate new images that resemble a given set of training images, useful in art, design, and entertainment.
	- **Objective**: Learn the underlying distribution of training images to generate new, plausible images.
	- **Loss Function**: Combination of reconstruction loss (e.g., Mean Squared Error) and Kullback-Leibler (KL) divergence to ensure the encoded latent space follows a specified distribution (usually a normal distribution).
- And the same other applications as simple Auto-Encoders