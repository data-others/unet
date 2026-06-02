# U-Net Models for Image Segmentation

## Introduction

This repository provides compressed `.nz` segmentation models for brain MRI segmentation. The current model collection includes human, marmoset, mouse, and rat models, and the repository is intended to support additional species and modalities as new models are added.

The models can be used by [DSI Studio](https://dsi-studio.labsolver.org) and [U-Net Studio](https://unet-studio.labsolver.org). They are designed to simplify image segmentation by providing ready-to-use models and template-based training models that can be adapted or retrained for different imaging modalities.

The repository includes two types of models:

1. **Converted third-party models**  
   These models were converted from existing third-party model weights, compressed into DSI Studio `.nz` format, and packaged for use in DSI Studio and U-Net Studio. The conversion may include changes in storage format, compression, metadata, and runtime packaging.

2. **U-Net Studio template-based training models**  
   These models were trained using U-Net Studio’s template-based training workflow. They are intended to support tissue, tumor, stroke, and animal brain segmentation across different MRI contrasts.

## Software

These models can be used with:

- [DSI Studio](https://dsi-studio.labsolver.org)
- [U-Net Studio](https://unet-studio.labsolver.org)

In DSI Studio, the models can be selected from the segmentation interface or specified in command-line workflows using the model name.

## License

The `.nz` model files in this repository are shared under the **DSI Studio License**.

Some `.nz` files are converted and compressed from third-party model weights. For these models, the redistributed `.nz` file bears the DSI Studio License for the DSI Studio-specific converted package, while the original model-derived material remains subject to the original third-party license.

Users must comply with both the DSI Studio License and the applicable original third-party license.

Converted third-party models include:

| Model | Original Project | Original License |
|---|---|---|
| TumorSynth | https://github.com/fprados/TumorSynth | TumorSynth Software License Agreement |
| SynthSeg V2 | https://github.com/BBillot/SynthSeg | Apache License 2.0 |
| SIAM | https://github.com/romainVala/SIAM | Apache License 2.0 |
| GOUHFI | https://github.com/mafortin/GOUHFI | Apache License 2.0 |
| MedNet-PVS | https://github.com/iBrain-Lab/MedNet-PVS | Apache License 2.0 |

Redistribution of converted models should include the model-specific license notice, the original license text, the DSI Studio License, and attribution to the original project.

The U-Net Studio template-based training models are distributed under the DSI Studio License unless otherwise specified.

The models are provided as is, without warranty of any kind, and are intended for research use unless separately permitted by the applicable licenses and laws. Users are responsible for validating each model for their own data, imaging protocol, and research application.

## Available Models

### Human

| Model | Description | Download |
|---|---|---|
| TumorSynth (20.7MB) | Converted TumorSynth model for segmenting healthy brain tissue and tumor in brain MRI scans with tumor. The original TumorSynth tool supports multi-sequence MRI inputs, including T1, contrast-enhanced T1/T1CE, T2, FLAIR, and related contrasts. The `.nz` package provides the converted model weights for use in DSI Studio. | [human_tumorsynth.nz](https://github.com/data-others/unet/releases/download/tumorsynth/human_tumorsynth.nz) |
| SynthSeg V2 (10.5MB) | Converted SynthSeg 2.0 model for contrast- and resolution-agnostic brain MRI segmentation. The original SynthSeg model was designed to work without retraining across diverse contrasts, resolutions, populations, and preprocessing conditions, including scans with white matter lesions. | [human_synthseg2.nz](https://github.com/data-others/unet/releases/download/synthseg/human_synthseg.nz) |
| SIAM Model 1 (64.1MB) | Converted SIAM Model 1 for full-head tissue segmentation. The original SIAM Model 1 performs a 39-region segmentation task and may be useful when extra-cerebral labels are needed. | [human_SIAM_model1.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model1.nz) |
| SIAM Model 2 (51.8MB) | Converted SIAM Model 2 for full-head tissue segmentation. The original SIAM Model 2 was trained from high-quality templates and targets brain tissue and head-related labels, including tissue, skull, dura, and vessel-related structures. | [human_SIAM_model2.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model2.nz) |
| SIAM Model 3 (21.5MB) | Converted SIAM Model 3 for full-head tissue segmentation with improved robustness to anatomical abnormalities. The original SIAM Model 3 extends SIAM Model 2 by adding support for anatomical anomalies as an additional label. | [human_SIAM_model3.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model3.nz) |
| GOUHFI (79.6MB) | Converted GOUHFI model for brain MRI segmentation. The original GOUHFI toolbox is a contrast-, resolution-, and field-strength-agnostic deep learning tool optimized for ultra-high-field MRI, with support for brain segmentation, cortical parcellation, and volumetric analysis depending on the model version. | [human_GOUHFI.nz](https://github.com/data-others/unet/releases/download/gouhfi/human_gouhfi.nz) |
| MedNet-PVS T2w (19.7MB) | Converted MedNet-PVS model for automated 3D perivascular space segmentation on T2-weighted brain MRI. The original T2w MedNet-PVS models were designed for white matter PVS segmentation and were trained on HCP Aging T2w MRI data. | [human_mednet_pvs_T2w.nz](https://github.com/data-others/unet/releases/download/mednet/human_mednet_pvs_T2w.nz) |
| U-Net Studio Human T1w Tissue (1.2MB) | U-Net Studio template-based tissue segmentation model for human T1-weighted MRI. This model is intended for lightweight tissue segmentation in DSI Studio and U-Net Studio workflows. | [human_tissue_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_T1w.nz) |
| U-Net Studio Human T2w Tissue (1.2MB) | U-Net Studio template-based tissue segmentation model for human T2-weighted MRI. This model is intended for tissue segmentation when T2w contrast is available. | [human_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_T2w.nz) |
| U-Net Studio Human FLAIR Tissue (1.3MB) | U-Net Studio template-based tissue segmentation model for human FLAIR MRI. This model supports tissue segmentation in FLAIR-based workflows. | [human_tissue_FLAIR.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_FLAIR.nz) |
| U-Net Studio Human T1w Stroke (1.2MB) | U-Net Studio template-based stroke segmentation model for human T1-weighted MRI. This model is intended for research workflows involving stroke-related lesion segmentation. | [human_stroke_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_stroke_T1w.nz) |
| U-Net Studio Human T1w Tumor (1.3MB) | U-Net Studio template-based tumor segmentation model for human T1-weighted MRI. This model is intended for research workflows involving tumor segmentation on non-contrast T1w scans. | [human_tumor_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_T1w.nz) |
| U-Net Studio Human T1w-gd Tumor (1.3MB) | U-Net Studio template-based tumor segmentation model for contrast-enhanced human T1-weighted MRI. This model is intended for research workflows using gadolinium-enhanced T1w images. | [human_tumor_gad_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_gad_T1w.nz) |
| U-Net Studio Human FLAIR Tumor (1.3MB) | U-Net Studio template-based tumor segmentation model for human FLAIR MRI. This model is intended for research workflows where tumor-related signal is evaluated on FLAIR images. | [human_tumor_FLAIR.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_FLAIR.nz) |

### Rhesus

| Model | Description | Download |
|---|---|---|
| U-Net Studio Rhesus Tissue V2 (13MB) | U-Net Studio model-agnostic tissue segmentation model for rhesus. | [rhesus_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/rhesus_tissue.nz) |


### Marmoset

| Model | Description | Download |
|---|---|---|
| U-Net Studio Marmoset T1w Tissue (1.3MB) | U-Net Studio template-based tissue segmentation model for marmoset T1-weighted MRI. This model supports animal brain segmentation workflows without requiring manual annotation for each new dataset. | [marmoset_tissue_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue_T1w.nz) |
| U-Net Studio Marmoset T2w Tissue (1.2MB) | U-Net Studio template-based tissue segmentation model for marmoset T2-weighted MRI. This model is intended for marmoset tissue segmentation using T2w contrast. | [marmoset_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue_T2w.nz) |
| U-Net Studio Marmoset Tissue V2 (13MB) | U-Net Studio model-agnostic tissue segmentation model for marmoset. | [marmoset_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue.nz) |


### Mouse

| Model | Description | Download |
|---|---|---|
| U-Net Studio Mouse T2w Tissue (1.3MB) | U-Net Studio template-based tissue segmentation model for mouse T2-weighted MRI. This model is intended for mouse brain tissue segmentation and can be used as a starting point for template-based retraining. | [mouse_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/mouse_tissue_T2w.nz) |

### Rat

| Model | Description | Download |
|---|---|---|
| U-Net Studio Mouse T2w Tissue (1.2MB) | U-Net Studio template-based tissue segmentation model for rat T2-weighted MRI. This model is intended for rat brain tissue segmentation and can be adapted or retrained for related animal MRI datasets. | [rat_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/rat_tissue_T2w.nz) |

## Model Format

The `.nz` files are compressed model packages used by DSI Studio and U-Net Studio. A model package may include:

- model weights
- architecture information
- preprocessing metadata
- label information
- DSI Studio-specific runtime metadata

For converted third-party models, the `.nz` file is a derived and compressed package based on the original model weights. The conversion changes the storage format, compression method, metadata, and runtime packaging for compatibility with DSI Studio and U-Net Studio. The converted `.nz` file should not be represented as the original model file.

## Usage

Download the desired `.nz` model file and place it in the model folder used by DSI Studio or U-Net Studio.

In DSI Studio, the model can be selected from the segmentation interface. If no model is specified, DSI Studio may list available models.

Example command-line usage:

```bash
dsi_studio --action=img \
           --source=input.nii.gz \
           --cmd="segment" \
           --model=human_tissue_T1w.nz
```

The exact command may depend on the DSI Studio version and the intended segmentation workflow.

## Citation and Attribution

If you use a converted third-party model, please cite or acknowledge the corresponding original project when appropriate:

- TumorSynth: https://github.com/fprados/TumorSynth
- SynthSeg: https://github.com/BBillot/SynthSeg
- SIAM: https://github.com/romainVala/SIAM
- GOUHFI: https://github.com/mafortin/GOUHFI
- MedNet-PVS: https://github.com/iBrain-Lab/MedNet-PVS

If you use DSI Studio or U-Net Studio in academic work, please cite the relevant DSI Studio or U-Net Studio publication or documentation.


## Disclaimer

These models are intended for research use unless separately permitted by the applicable licenses and laws.

The models are provided as is, without warranty of any kind. No claim is made that the models are suitable for clinical diagnosis, treatment planning, regulatory use, or commercial deployment unless such use is separately permitted by the applicable licenses, institutional policies, and laws.

Users are responsible for validating the models for their own data, imaging protocols, and research applications.

## Contact

For questions about DSI Studio or U-Net Studio model use, please refer to:

- DSI Studio: https://dsi-studio.labsolver.org
- U-Net Studio: https://unet-studio.labsolver.org