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
