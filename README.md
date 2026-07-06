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
| SynthSeg V2 (10.5MB)                    | Anatomy segmentation for human brain MRI. Contrast- and resolution-agnostic; provides 32 anatomical labels plus background, including cortex, white matter, ventricles, cerebellum, deep nuclei, brainstem, CSF, hippocampus, and amygdala. | [human_synthseg2.nz](https://github.com/data-others/unet/releases/download/synthseg/human_synthseg.nz)           |
| SIAM Model 1 (64.1MB)                   | Full-head tissue segmentation for 3D human head images. Contrast-, resolution-, and pathology-robust; provides 39 head tissue regions, including extra-cerebral labels.                                                                     | [human_SIAM_model1.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model1.nz)          |
| SIAM Model 2 (51.8MB)                   | Full-head tissue segmentation for 3D human head images. Contrast-, resolution-, and pathology-robust; provides 12 brain tissue labels plus head, skull, dura, and vessel-related labels.                                                    | [human_SIAM_model2.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model2.nz)          |
| SIAM Model 3 (21.5MB)                   | Full-head tissue segmentation for 3D human head images with anomaly support. Extends SIAM Model 2 by adding an anomaly-related label for abnormal anatomy.                                                                                  | [human_SIAM_model3.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model3.nz)          |
| GOUHFI (79.6MB)                         | Brain segmentation and volumetric analysis for human MRI. Contrast-, resolution-, and field-strength-agnostic; GOUHFI 2.0 provides 35-label whole-brain segmentation and a separate 62-label DKT cortical parcellation task.                | [human_GOUHFI.nz](https://github.com/data-others/unet/releases/download/gouhfi/human_gouhfi.nz)                  |
| MedNet-PVS T2w (19.7MB)                 | Perivascular space segmentation for human T2-weighted MRI. Modality-specific; trained on HCP-Aging T2w scans and provides white matter PVS segmentation only.                                                                               | [human_mednet_pvs_T2w.nz](https://github.com/data-others/unet/releases/download/mednet/human_mednet_pvs_T2w.nz)  |
| U-Net Studio Human Tissue (13MB)        | Five-tissue segmentation for human structural MRI. Contrast-flexible model supporting common inputs such as T1w, T2w, FLAIR, and related structural MRI contrasts.                                                                          | [human_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue.nz)             |
| U-Net Studio Human T1w Tissue (1.2MB)   | Five-tissue segmentation for human T1-weighted MRI. Modality-specific lightweight model optimized for T1w tissue-label workflows.                                                                                                           | [human_tissue_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_T1w.nz)     |
| U-Net Studio Human T2w Tissue (1.2MB)   | Five-tissue segmentation for human T2-weighted MRI. Modality-specific lightweight model optimized for T2w tissue-label workflows.                                                                                                           | [human_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_T2w.nz)     |
| U-Net Studio Human FLAIR Tissue (1.3MB) | Five-tissue segmentation for human FLAIR MRI. Modality-specific lightweight model optimized for FLAIR tissue-label workflows.                                                                                                               | [human_tissue_FLAIR.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_FLAIR.nz) |

### Human Diseases

| Model | Description | Download |
|---|---|---|
| TumorSynth (20.7MB)                          | Brain tumor segmentation for multi-sequence MRI with tumor. Supports T1, T1CE, T2, FLAIR, and related inputs, and provides tumor/tissue segmentation for brain tumor scans.                                                 | [human_tumorsynth.nz](https://github.com/data-others/unet/releases/download/tumorsynth/human_tumorsynth.nz)        |
| MindGlide MS Lesion (25MB)                   | MS lesion and brain-structure segmentation for real-world brain MRI. Modality-agnostic model designed for variable scan quality; provides 19 output labels plus background, including lesion and major brain-region labels. | [human_mindglide.nz](https://github.com/data-others/unet/releases/download/mindglide/human_mindglide.nz)           |
| U-Net Studio Human Tumor Lesion V2 (13MB)    | Tumor lesion segmentation for human structural MRI. Contrast-flexible model supporting common tumor MRI inputs such as T1w, T1w-gd, T2w, FLAIR, and related contrasts.                                                      | [human_tumor.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor.nz)                 |
| U-Net Studio Human T1w Tumor Lesion (1.3MB)  | Tumor lesion segmentation for human T1-weighted MRI. Modality-specific lightweight model optimized for non-contrast T1w tumor-lesion workflows.                                                                             | [human_tumor_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_T1w.nz)         |
| U-Net Studio Human T1w-gd Tumor (1.3MB)      | Tumor lesion segmentation for contrast-enhanced human T1-weighted MRI. Modality-specific lightweight model optimized for gadolinium-enhanced T1w tumor-lesion workflows.                                                    | [human_tumor_gad_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_gad_T1w.nz) |
| U-Net Studio Human FLAIR Tumor (1.3MB)       | Tumor lesion segmentation for human FLAIR MRI. Modality-specific lightweight model optimized for FLAIR-based tumor-lesion workflows.                                                                                        | [human_tumor_FLAIR.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_FLAIR.nz)     |
| U-Net Studio Human Stroke Lesion V2 (13MB)   | Stroke lesion segmentation for human structural MRI. Contrast-flexible model supporting common stroke MRI inputs such as T1w, T2w, FLAIR, and related contrasts.                                                            | [human_stroke.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_stroke.nz)               |
| U-Net Studio Human MS Lesion V2 (13MB)       | Multiple sclerosis lesion segmentation for human structural MRI. Contrast-flexible model supporting common MS MRI inputs such as T1w, T2w, FLAIR, and related contrasts.                                                    | [human_ms.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_ms.nz)                       |
| U-Net Studio Human T1w Stroke Lesion (1.2MB) | Stroke lesion segmentation for human T1-weighted MRI. Modality-specific lightweight model optimized for T1w stroke-lesion workflows.                                                                                        | [human_stroke_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_stroke_T1w.nz)       |


### Rhesus

| Model | Description | Download |
|---|---|---|
| U-Net Studio Rhesus Tissue V2 (13MB) | U-Net Studio model-agnostic tissue segmentation model for rhesus. | [rhesus_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/rhesus_tissue.nz) |

### Marmoset

| Model | Description | Download |
|---|---|---|
| U-Net Studio Marmoset Tissue V2 (13MB) | U-Net Studio model-agnostic tissue segmentation model for marmoset MRI (T1w,T2w,FLAIR...etc). | [marmoset_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue.nz) |
| U-Net Studio Marmoset T1w Tissue (1.3MB) | U-Net Studio template-based tissue segmentation model for marmoset T1-weighted MRI. This model supports animal brain segmentation workflows without requiring manual annotation for each new dataset. | [marmoset_tissue_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue_T1w.nz) |
| U-Net Studio Marmoset T2w Tissue (1.2MB) | U-Net Studio template-based tissue segmentation model for marmoset T2-weighted MRI. This model is intended for marmoset tissue segmentation using T2w contrast. | [marmoset_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue_T2w.nz) |


### Mouse

| Model | Description | Download |
|---|---|---|
| U-Net Studio Mouse Tissue V2 (13MB) | U-Net Studio model-agnostic tissue segmentation model for mouse MRI. | [mouse_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/mouse_tissue.nz) |
| U-Net Studio Mouse T2w Tissue (1.3MB) | U-Net Studio template-based tissue segmentation model for mouse T2-weighted MRI. This model is intended for mouse brain tissue segmentation and can be used as a starting point for template-based retraining. | [mouse_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/mouse_tissue_T2w.nz) |

### Rat

| Model | Description | Download |
|---|---|---|
| U-Net Studio Rat Tissue V2 (13MB) | U-Net Studio model-agnostic tissue segmentation model for rat MRI. | [rat_tissue.nz](https://github.com/data-others/unet/releases/download/unet-studio/rat_tissue.nz) |
| U-Net Studio Rat T2w Tissue (1.2MB) | U-Net Studio template-based tissue segmentation model for rat T2-weighted MRI. This model is intended for rat brain tissue segmentation and can be adapted or retrained for related animal MRI datasets. | [rat_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/rat_tissue_T2w.nz) |

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
