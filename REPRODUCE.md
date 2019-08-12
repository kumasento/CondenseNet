# Reproducibility Report

## On CIFAR-10 and CIFAR-100

```shell
# CIFAR-10
python main.py $NAS_HOME/datasets --model condensenet -b 64 -j 8 cifar10 --epochs 300 --lr-type cosine --stages 14-14-14 --growth 8-16-32 --bottleneck 4 --group-1x1 4 --group-3x3 4 --condense-factor 4 --gpu 0 --resume --savedir $NAS_HOME/train/condensenet/condensenet86/cifar10/baseline --manual-seed 42
# CIFAR-100
python main.py $NAS_HOME/datasets --model condensenet -b 64 -j 8 cifar100 --epochs 300 --lr-type cosine --stages 14-14-14 --growth 8-16-32 --bottleneck 4 --group-1x1 4 --group-3x3 4 --condense-factor 4 --gpu 0 --resume --savedir $NAS_HOME/train/condensenet/condensenet86/cifar100/baseline --manual-seed 42
```