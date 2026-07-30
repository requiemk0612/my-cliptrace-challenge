---
pretty_name: CLIPTrace 2026 Baseline Data
license: other
task_categories:
  - image-classification
language:
  - en
tags:
  - imagenette
  - clip
  - backdoor-detection
  - cliptrace-2026
size_categories:
  - 10K<n<100K
---

# CLIPTrace 2026 Baseline Data

Participant data for the reproducible CLIPTrace 2026 baseline. The repository
mirrors the full-size Imagenette train and validation images used by the
baseline and preserves the original class-directory layout.

This repository is intended to be **public with access gating**. Before
downloading, users must accept the repository terms and the upstream image-use
conditions configured by the organizers on the Hugging Face settings page.

## Dataset summary

| Split | Images | Classes |
|---|---:|---:|
| train | 9,469 | 10 |
| validation | 3,925 | 10 |
| total | 13,394 | 10 |

Expected layout:

```text
imagenet/
  train/
    n01440764/
    ...
  val/
    n01440764/
    ...
manifest/
  files.sha256
  dataset-summary.json
```

The baseline uses a seeded, recorded subset of `imagenet/val`. Labels are not
used by the trigger-inversion objective but the class folders are preserved for
provenance and compatibility with `ImageFolder`.

## Source and rights

Imagenette was prepared by fast.ai as a small, easily usable subset of ImageNet.
See the [upstream Imagenette repository](https://github.com/fastai/imagenette)
for its description and download information.

The images originate from ImageNet. The dataset repository does not grant new
rights in the images. Users are responsible for complying with the
[ImageNet terms of access and use](https://www.image-net.org/download.php),
research-only restrictions where applicable, and any rights associated with
individual images. Access may be revoked if the data is redistributed or used
outside the accepted terms.

## Integrity and reproducibility

`manifest/files.sha256` records the SHA-256 digest of every image using POSIX
relative paths. `manifest/dataset-summary.json` records file counts by split and
class. Generate both with the baseline repository's
`tools/build_dataset_manifest.py`; verify them again after Hub download before
running a formal experiment.

## Personal and sensitive information

Imagenette includes ordinary photographs selected from ImageNet. Some images
may incidentally contain people. The organizers have not performed identity or
consent annotation. Do not use this mirror for face recognition, identity
inference, surveillance, or other decisions about individuals.

## Citation

Please cite the upstream Imagenette project and ImageNet when using these
images, and cite the CLIPTrace 2026 baseline repository when reporting results
obtained with its deterministic sampling protocol.

