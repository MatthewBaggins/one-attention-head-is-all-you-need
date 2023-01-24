# models

- `model_{n}.pkl` - state dict of the model trained in notebook `n` (in `notebooks`)
- `models_4.pkl` - dictionary of state dicts of 0-layer models trained in notebook `4` with different list lengths and vocab sizes, indexed by tuples (`d_vocab`, `list_length`)
- `training_histories_4.pkl` - dictionary of `TrainingHistory`'ies of models from notebook `4`, also indexed by tuples (`d_vocab`, `list_length`)
