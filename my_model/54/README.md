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
    "epoch": 54,
    "IOU": 0.5596405267715454,
    "accuracy": 0.935859739780426,
    "F1": 0.8541914820671082,
    "Precision": 0.9812188744544983,
    "Recall": 0.7611904144287109,
    "Dice": 0.15617869794368744
}
```

## Dataset
Dataset name: [More Information Needed]

## More Information
- Library: https://github.com/qubvel/segmentation_models.pytorch
- Docs: https://smp.readthedocs.io/en/latest/

This model has been pushed to the Hub using the [PytorchModelHubMixin](https://huggingface.co/docs/huggingface_hub/package_reference/mixins#huggingface_hub.PyTorchModelHubMixin)