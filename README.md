# training template

A advanced pytorch model training template, aiming to form an efficient and scentific template for futher use.

## key features
- [x] distributed training
- [x] enable lr_scheduler, dynamic adjust learning rate
- [x] gradient accumulation
- [x] mixed precision training
- [x] self-formated dataset
- [x] use train-config file to conduct training
- [x] logging, record whole train process
- [ ] tensorboard

## file tree expalained

```python
.
├── README.md
├── config (# the training config file)
│   └── xxxx.yaml
├── data (# datasets and model files, git ignore)
│   ├── dataset (# dataset files)
│   └── model (# model files)
├── scripts (# scripts that is not directly used in training)
├── src (# source code used to train)
│   ├── data (# form the self-defined datasets)
│   │   ├── PretrainDataset.py
│   │   └── ...
│   ├── metric (# evaluation tools)
│   │   ├── metric.py
│   │   └── ...
│   ├── models (# model structure files)
│   │   ├── proposed_model.py
│   │   └── ...
│   ├── lr_scheduler.py (# learning rate scheduler)
│   └── util.py (# scripts used in training)
├── log (# all logs)
│   ├── train.log
│   └── test.log
├── distributed.py (# distributed utils)
├── test.py
└── train.py
```