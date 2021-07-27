# OMRL for `jacopinpad`
To install run `pip install -e .`. You need to install `mojuco-py`.
# Generate Demo
```
python main.py --mode demo --sketch_lengths 4 --demo_episodes 1400
```
The dataset is generated under the `dataset` folder.
# OMPN
```
# No supervision
python main.py --mode IL --arch omstack --flagfile ilflagfile --nb_slots 2 --cuda --sketch_lengths 4 --env_arch noenv --il_lr 0.0005

# Sketch supervision
python main.py --mode IL --arch omstack --flagfile ilflagfile --nb_slots 2 --cuda --sketch_lengths 4 --env_arch sketch --il_lr 0.0005

```

# Evaluate structure
```
python scripts/structure_eval.py --model_ckpt <CKPT_PATH> --sketch_lengths 4
```

# Visualize
```
python scripts/visualize.py --sketch_lengths 4 --episodes 20 --model_ckpt <CKPT_PATH>
```
