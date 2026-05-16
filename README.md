# U-Net Models for Image Segmentation

## Introduction

This repository provides `.nz` segmentation models for brain MRI segmentation in mouse, rat, marmoset, rhesus monkey, and human imaging data.

The models can be used by [DSI Studio](https://dsi-studio.labsolver.org) and [U-Net Studio](https://unet-studio.labsolver.org). They are designed to simplify image segmentation by providing ready-to-use models and template-based training models that can be adapted or retrained for different imaging modalities.

The repository includes two types of models:

1. **Converted third-party models**  
   These models were converted from existing model weights, compressed into DSI Studio `.nz` format, and packaged for use in DSI Studio and U-Net Studio.

2. **U-Net Studio template-based training models**  
   These models were trained using U-Net Studio’s template-based training approach. They are intended to support tissue, tumor, stroke, and animal brain segmentation across different MRI contrasts.

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
| SIAM Models | https://github.com/romainVala/SIAM | Apache License 2.0 |
| GOUHFI | https://github.com/mafortin/GOUHFI | Apache License 2.0 |

Redistribution of converted models should include the model-specific license notice, the original license text, the DSI Studio License, and attribution to the original project.

The U-Net Studio template-based training models are distributed under the DSI Studio License unless otherwise specified.

The models are provided as is, without warranty of any kind, and are intended for research use unless separately permitted by the applicable licenses and laws.

## Available Models

### Human

| Model | Description | Download |
|---|---|---|
| TumorSynth (20.7MB)  | Converted TumorSynth model for brain tumor and tissue segmentation | [human_tumorsynth.nz](https://github.com/data-others/unet/releases/download/tumorsynth/human_tumorsynth.nz) |
| SynthSeg V2 (10.5MB) | Converted SynthSeg 2.0 model for brain segmentation | [human_synthseg2.nz](https://github.com/data-others/unet/releases/download/synthseg/human_synthseg.nz) |
| SIAM Model 1 (64.1MB) | Converted SIAM model | [human_SIAM_model1.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model1.nz) |
| SIAM Model 2 (51.8MB) | Converted SIAM model | [human_SIAM_model2.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model2.nz) |
| SIAM Model 3 (21.5MB) | Converted SIAM model | [human_SIAM_model3.nz](https://github.com/data-others/unet/releases/download/siam/human_siam_model3.nz) |
| GOUHFI (79.6MB) | Converted GOUHFI model | [human_GOUHFI.nz](https://github.com/data-others/unet/releases/download/gouhfi/human_gouhfi.nz) |
| U-Net Studio T1w Tissue (1.2MB) | Template-based tissue segmentation model for T1w MRI | [human_tissue_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_T1w.nz) |
| U-Net Studio T2w Tissue (1.2MB) | Template-based tissue segmentation model for T2w MRI | [human_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_T2w.nz) |
| U-Net Studio FLAIR Tissue (1.3MB) | Template-based tissue segmentation model for FLAIR MRI | [human_tissue_FLAIR.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tissue_FLAIR.nz) |
| U-Net Studio T1w Stroke (1.2MB) | Template-based stroke segmentation model for T1w MRI | [human_stroke_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_stroke_T1w.nz) |
| U-Net Studio T1w Tumor (1.3MB) | Template-based tumor segmentation model for T1w MRI | [human_tumor_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_T1w.nz) |
| U-Net Studio T1w-gd Tumor (1.3MB) | Template-based tumor segmentation model for contrast-enhanced T1w MRI | [human_tumor_gad_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_gad_T1w.nz) |
| U-Net Studio FLAIR Tumor (1.3MB) | Template-based tumor segmentation model for FLAIR MRI | [human_tumor_FLAIR.nz](https://github.com/data-others/unet/releases/download/unet-studio/human_tumor_FLAIR.nz) |

### Marmoset

| Model | Description | Download |
|---|---|---|
| U-Net Studio T1w Tissue (1.3MB) | Template-based marmoset tissue segmentation model for T1w MRI | [marmoset_tissue_T1w.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue_T1w.nz) |
| U-Net Studio T2w Tissue (1.2MB) | Template-based marmoset tissue segmentation model for T2w MRI | [marmoset_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/marmoset_tissue_T2w.nz) |

### Mouse

| Model | Description | Download |
|---|---|---|
| U-Net Studio T2w Tissue (1.3MB) | Template-based mouse tissue segmentation model for T2w MRI | [mouse_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/mouse_tissue_T2w.nz) |

### Rat

| Model | Description | Download |
|---|---|---|
| U-Net Studio T2w Tissue (1.2MB) | Template-based rat tissue segmentation model for T2w MRI | [rat_tissue_T2w.nz](https://github.com/data-others/unet/releases/download/unet-studio/rat_tissue_T2w.nz) |

## Usage

Download the desired `.nz` model file and place it in the model folder used by DSI Studio or U-Net Studio.

In DSI Studio, the model can be selected from the segmentation interface. If no model is specified, DSI Studio may list available models.

Example command-line usage:

```bash
dsi_studio --action=img \
           --source=input.nii.gz \
           --cmd="segment" \
           --model=human_tissue_T1w.nz
