# evaluate-performance
evaluate performance of different GAN networks

## Extract attributes
Using a pretrained network for detecting if the person in an image is male or female.

## SSIM Score
For evaluating if the GAN produces diverse results we can use the Structural Similarity Index Metric.

## Incpetion Score
1.Train an Inception classifier on a reference dataset (e.g., ImageNet) to learn how to classify images into various categories.
2.Generate a set of images using the GAN that we want to evaluate.
3.Calculate the feature vectors (embeddings) for the generated images using the pretrained Inception classifier's layer.
4.Compute the mean and covariance matrix of the feature vectors of the generated images.
5.Calculate the Inception score as the sum of the mean of the feature vectors of the generated images and the product of their covariance matrix and the reference matrix (mean and covariance matrix of the feature vectors of reference images from the ImageNet dataset).
6.A higher Inception score indicates that the generated images are considered more diverse and realistic.

## Frechet Incpetion Distance
The Frechet Inception Distance (FID) is a measure used to evaluate the similarity between the distribution of real images and generated images. It uses the feature embeddings from a pretrained Inception network to calculate the distance between the two distributions. A lower FID indicates a better similarity between the distributions of real and generated images.
