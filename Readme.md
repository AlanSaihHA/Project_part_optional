# Tensors and invariants, duct flow case


This code will compute the tensors and invariants for the square duct case used by [Ling(2016)](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/abs/reynolds-averaged-turbulence-modelling-using-deep-neural-networks-with-embedded-invariance/0B280EEE89C74A7BF651C422F8FBD1EB) to train a neural network, the raw data is obtained from [here](https://www.kaggle.com/ryleymcconkey/ml-turbulence-dataset/version/1).


## Raw data

The raw data is for the duct flow case Re<sub>b</sub>=3500 (kepsilon model), the datasets used are:

(from kepsilon folder)

* kepsilon_DUCT_3500_epsilon.npy
* kepsilon_DUCT_3500_gradU.npy
* kepsilon_DUCT_3500_k.npy

(from /labels/orig folder)
* DUCT_3500_uu.npy
* DUCT_3500_uv.npy
* DUCT_3500_uw.npy
* DUCT_3500_vv.npy
* DUCT_3500_vw.npy
* DUCT_3500_ww.npy

*Note: due to the symmetric nature of the strain rate tensor only 6 components are needed*

## Preprocessing 

Sorting the data is needed before finding the tensors and invariants, with the data gathered we can build 9216 cases each one with 20 inputs. for this code the order of this inputs are: k, epsilon, grad_u_00, grad_u_01, grad_u_02, grad_u_10, grad_u_11, grad_u_12, grad_u_20, grad_u_21, grad_u_22, uu, uv, uw, uv, vv, vw, uw, vw, ww.

## Postprocessing 

The full algorithm to obtain the tensors and invariants is described in [Ling(2016)](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/abs/reynolds-averaged-turbulence-modelling-using-deep-neural-networks-with-embedded-invariance/0B280EEE89C74A7BF651C422F8FBD1EB).