---
library_name: segmentation-models-pytorch
license: mit
pipeline_tag: image-segmentation
tags:
- model_hub_mixin
- pytorch_model_hub_mixin
- segmentation-models-pytorch
- semantic-segmentation
- pytorch
languages:
- python
---
# Unet Model Card

Table of Contents:
- [Load trained model](#load-trained-model)
- [Model init parameters](#model-init-parameters)
- [Model metrics](#model-metrics)
- [Dataset](#dataset)

## Load trained model
```python
import segmentation_models_pytorch as smp

model = smp.from_pretrained("<save-directory-or-this-repo>")
```

## Model init parameters
```python
model_init_params = {
    "encoder_name": "efficientnet-b0",
    "encoder_depth": 5,
    "encoder_weights": None,
    "decoder_use_norm": "batchnorm",
    "decoder_channels": (256, 128, 64, 32, 16),
    "decoder_attention_type": None,
    "decoder_interpolation": "bilinear",
    "in_channels": 3,
    "classes": 2,
    "activation": None,
    "aux_params": None
}
```

## Model metrics
```json
{
    "epoch": 74,
    "IOU": 0.743619978427887,
    "accuracy": 0.9659698009490967,
    "F1": 0.9311413764953613,
    "Precision": 0.8914123773574829,
    "Recall": 0.9299744367599487,
    "Dice": 0.11126185953617096
}
```

## Dataset
Dataset name: [More Information Needed]

## More Information
- Library: https://github.com/qubvel/segmentation_models.pytorch
- Docs: https://smp.readthedocs.io/en/latest/

This model has been pushed to the Hub using the [PytorchModelHubMixin](https://huggingface.co/docs/huggingface_hub/package_reference/mixins#huggingface_hub.PyTorchModelHubMixin)