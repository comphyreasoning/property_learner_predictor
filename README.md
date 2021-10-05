# Physical Property Learner and Dynamic Predictor
 This repo contains the physical property learner and the physics-based dynamic predictor of the Compositional Physics Learner in [ComPhy](https://comphyreasoning.github.io).

### Data preparation
- Download training and validation object tracks of [target videos](https://drive.google.com/file/d/1Qbkowx1Xph-70L5gDPVNn5Ba-lkpOaLg/view?usp=sharing) and [reference videos](https://drive.google.com/file/d/1e0oC7Bo41YZxj8lXTi4DlYdwy-9cNx8M/view?usp=sharing) extracted from Mask-RCNN;
- Download testing object tracks of [target videos](https://drive.google.com/file/d/1B4Kq0rda1BGGNVEe5ULB0ckuL258RE5i/view?usp=sharing) and [reference videos](https://drive.google.com/file/d/1pvXXMCMoMin6liVmHMmCK25gVfiLDmne/view?usp=sharing) extracted from Mask-RCNN.

### Run experiments on physical property learning
Train mass predictor
```
sh scripts/train_mass_property_prp.sh
```
Train charge predictor
```
sh scripts/train_charge_property_prp.sh
```
Evaluate on validation set of  mass predictor
```
sh scripts/test_mass_property.sh
```
Evaluate on validation set of charge predictor
```
sh scripts/test_charge_property.sh
```

### Run experiments on dynamic prediction
process output of physical property learner for dynamic predictor
```
sh scripts/post_processing_prp.sh
```
Train dynamic predictor
```
sh scripts/train_dynamic_predictor.sh
```
Test on dynamic predictor
```
sh scripts/test_dynamic_predictor.sh
```

### Acknowledgement
Much code is borrowed from Thomas Kipf's [NRI repo](https://github.com/ethanfetaya/NRI.git).
