# dynamics-sample-reduction
Dependencies:
- notebook
- numpy
- matplotlib
- torch
- scipy

## Results
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
| 7i_conv_pool_lrelu_05 | 49.81% | 4*4 |
| 7i_conv_pool_rrelu | 49.79% | 4*4 |
| 6i_conv_pool_lrelu_05 | 53.18% | 5*5 |
| 6i_conv_pool_rrelu | 53.17% | 5*5 |
| 6i_conv_pool_lrelu_1 | 53.21% | 5*5 |
| 6i_conv_pool_lrelu_025 | 53.18% | 5*5 |
