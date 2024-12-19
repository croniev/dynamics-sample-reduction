# dynamics-sample-reduction
Dependencies:
- notebook
- numpy
- matplotlib
- torch
- scipy

## Results Dynamic Reduce
These Results are all for an approach where the data is only once converted to its fourier transform and all convolution and pooling is applied in this feature space.  
Transforming the results back to image does not significantly change performance as the fourier transform is linear.  

| Parameters | Accuracy | Input Size |
|------------|----------|------------|
| unreduced | 97.92% | 28*28 |
| 18i_conv_tanh | 38% | 10*10 |
| 24i_conv_tanh | 23% | 4*4 |
| 18i_conv_relu | 43.89% | 10*10 |
| 7i_conv_pool_tanh | 24.29% | 4*4 |
| 7i_conv_pool_relu | 49.67% | 4*4 |
| 6i_conv_pool_tanh | 31.1% | 5*5 |
| 6i_conv_pool_relu | 53.3% | 5*5 |
| 6i_conv_pool_relu (transformed back to image) | 52.53% | 5*5 |
| 6i_conv_pool_relu_v1 | 53.3% | 5*5 |
| 7i_conv_pool_lrelu_05 | 49.81% | 4*4 |
| 7i_conv_pool_rrelu | 49.79% | 4*4 |
| 6i_conv_pool_lrelu_05 | 53.18% | 5*5 |
| 6i_conv_pool_rrelu | 53.17% | 5*5 |
| 6i_conv_pool_lrelu_1 | 53.21% | 5*5 |
| 6i_conv_pool_lrelu_025 | 53.18% | 5*5 |
| 6i_conv_pool_elu_05 | 53.22% | 5*5 |
| multi5_9i_conv_pool_relu | 23.39% | 20 |
| multi5_7i_conv_pool_relu | 32.83% | 80 |
| 6i_conv_lppool3_relu | 29.24% | 5*5 |
| 6i_conv_mixedpool05_relu | 35.34% | 5*5 |
| 6i_conv_mixedpool08_relu | 35.24% | 5*5 |
| 6i_conv_mixedpool02_relu | 35.14% | 5*5 |

## Results Dynamic PCA
For these experiments I used only the training data. For testing, I split it at the 85% mark.  
Datasets with `pool` were converted back to image space before PCA. The number indicates how many pool-separated phases there were for each sample reduction (i.e. `pool1` = no pool, but `pool1` does PCA in img space and no pool does PCA in freq space).  
| Parameters | Accuracy | Input Size | Amount of Data |
|------------|----------|------------|----------------|
| unreduced | 97.92% | 28*28 | 1/1 |
| pca15_15i_relu | 88.11% | 15 | 1/1 |
| pca15_15i_relu | 84.03% | 15 | 1/3 |
| pca15_15i_relu_pool1 | 94.64% | 15 | 1/1 |
| pca15_15i_relu_pool1 | 93.33% | 15 | 1/3 |
| pca15_15i_relu_pool2 | 88.5% | 15 | 1/3 |
| pca15_15i_relu_pool3 | 71% | 15 | 1/3 |
| pca15_15i_relu_pool4 | 55.47% | 15 | 1/3 |
| pca15_15i_tanh | 79.5% | 15 | 1/3 |
| pca15_15i_tanh_pool1 | 90.8% | 15 | 1/3 |
| pca15_15i_tanh_pool2 | 83.97% | 15 | 1/3 |
| pca15_15i_tanh_pool3 | 61.93% | 15 | 1/3 |
