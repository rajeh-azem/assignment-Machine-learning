# assignment_Machine-learning
polynomial-regression
## Results (test set)

| Optimizer | RMSE | R2 |
|---|---|---|
| GD | 3.86 | 0.843 |
| SGD | 3.78 | 0.849 |
| Mini-Batch GD | 3.80 | 0.848 |
| RMSprop | 4.17 | 0.816 |
| Adam | 5.40 | 0.692 |

SGD and Mini-Batch got the best results here, and GD was very close. RMSprop and Adam needed more tuning (a smaller learning rate and more epochs) to reach the same level.

## Optimizers

| Optimizer | Update rule |
|---|---|
| Batch GD | `w = w - lr * grad(all data)` |
| SGD | `w = w - lr * grad(one sample)` |
| Mini-batch GD (batch 32) | `w = w - lr * grad(batch of 32)` |
| Momentum (beta 0.9) | `v = beta*v + g`, `w = w - lr*v` |
| Adam (b1 0.9, b2 0.999) | `m`, `v` moving averages with bias correction, `w = w - lr * m_hat / (sqrt(v_hat) + eps)` |

**Shared settings (same in all 5 notebooks):** `EPOCHS = 100`, `LR = 0.1`, `BATCH_SIZE = 32`, `SEED = 42`, `N_TREES = 25`, `MAX_DEPTH = 6`, `MIN_SAMPLES_SPLIT = 20`, `MIN_LEAF = 5`.
