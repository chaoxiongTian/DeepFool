# DeepFool
DeepFool is a simple algorithm to find the minimum adversarial perturbations in deep networks

###adversarial_perturbation.m

This function implements the algorithm proposed in [[1]](http://arxiv.org/pdf/1511.04599) to find the adverasrial perturbation.

###adversarial_DeepFool_matconvnet.m

This function is a wrapper to compute the adversarial perturbation for [MatConvNet](http://www.vlfeat.org/matconvnet/)'s models.

###adversarial_DeepFool_caffe.m

This function is a wrapper to compute the adversarial perturbation for [Caffe](http://caffe.berkeleyvision.org)'s models.

The arguments for both wrappers are:

- `x`: input image in `W*H*C` format
- `net`: network model where the last layer (loss) is removed.
- `opts`: a structure which contains two fields:
  - `labels_limit`: limits the number of classes to test against (default = 10).
  - `overshoot`: used as a termination criterion to prevent vanishing updates (default = 0.02).