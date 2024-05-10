# Adapted for BLUPF90 family program outputs

## A simple single trait model with only one random effect (additive animal effect only)

Find three components from BLUPF90+/AIREML/REML log files
  1) Genetic Variance for effect 5 (pedigree file name also contains the same number as renadd05.ped)  
  2) Residual Variance(s) (It is termed as R_1_1. Here _1_1 means trait 1. You must put two 1's here, either for a single or higher trait models.)

* Warning: Do not put a blank space before or after a particular component.
  
```sh
OPTION se_covar_function Vg G_5_5_1_1
OPTION se_covar_function Vp G_5_5_1_1+R_1_1
OPTION se_covar_function h2 G_5_5_1_1/(G_5_5_1_1+R_1_1)
```


