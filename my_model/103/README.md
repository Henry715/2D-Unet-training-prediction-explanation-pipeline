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
    "epoch": 103,
    "IOU": 0.7371165752410889,
    "accuracy": 0.9640611410140991,
    "F1": 0.9287897944450378,
    "Precision": 0.8568669557571411,
    "Recall": 0.947384774684906,
    "Dice": 0.11268065869808197
}
```

## Dataset
Dataset name: [More Information Needed]

## More Information
- Library: https://github.com/qubvel/segmentation_models.pytorch
- Docs: https://smp.readthedocs.io/en/latest/

This model has been pushed to the Hub using the [PytorchModelHubMixin](https://huggingface.co/docs/huggingface_hub/package_reference/mixins#huggingface_hub.PyTorchModelHubMixin)