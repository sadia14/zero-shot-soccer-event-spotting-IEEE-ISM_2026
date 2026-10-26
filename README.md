# Zero-Shot Multimodal Event Spotting in Soccer Broadcasts

This repository provides the resources accompanying the paper:

**Zero-Shot Multimodal Event Spotting in Soccer Broadcasts**

Sadia Kamal, Mahmudul Hasan, and Tony Braskich.

## Overview

This work investigates zero-shot soccer event spotting using general-purpose multimodal models without task-specific parameter fine-tuning. Full-length soccer broadcasts are segmented into overlapping clips and represented using sparse visual storyboards together with aligned commentary transcripts.

The evaluation consists of three professionally produced soccer broadcasts manually annotated for temporal event intervals.

## Event Categories

The evaluation uses six event categories:

- Goal
- Shot
- Miss
- Corner
- Kickoff
- Yellow Card

Across the three matches, the dataset contains **130 manually annotated ground-truth events**.

## Repository Contents

```text
.
├── README.md
├── video_urls.csv
├── annotations/
│   ├── betis_vs_barcelona.xlsx
│   ├── city_vs_liverpool.xlsx
│   └── city_vs_united.xlsx
└── metadata/
    └── event_taxonomy.csv
```

### `video_urls.csv`

Contains the public source URL for each evaluated soccer broadcast together with the corresponding match identifier and match name.

### `annotations/`

Contains the manually created temporal event annotations used for evaluation. Each annotation file corresponds to one full-length match.

The annotations contain event categories and their associated temporal locations or intervals in the original broadcast timeline.

### `metadata/event_taxonomy.csv`

Defines the six event categories used in the evaluation.

## Videos

The original soccer broadcast videos are **not redistributed in this repository**.

Instead, `video_urls.csv` provides links to the publicly available source videos used in the experiments. Availability of external videos is controlled by the original hosting platform and content owners.

## Evaluation Setting

Predicted event timestamps are evaluated against manually annotated temporal intervals. A prediction is considered temporally matched when it falls within the annotated interval or within the evaluation tolerance defined in the paper.

Predictions are temporally consolidated before final event-level evaluation to remove repeated detections caused by overlapping clips.

Please refer to the paper for the complete evaluation protocol, model configurations, temporal consolidation procedure, and reported metrics.

## Citation

If you use these annotations or resources, please cite:

```bibtex
@inproceedings{kamal2027zeroshot,
  title={Zero-Shot Multimodal Event Spotting in Soccer Broadcasts},
  author={Kamal, Sadia and Hasan, Mahmudul and Braskich, Tony},
  year={2027}
}
```

The citation information will be updated after publication.

## License and Data Usage

The annotations and metadata in this repository are provided for research and reproducibility purposes.

Copyright for the linked soccer broadcasts remains with the respective content owners. This repository does not redistribute or claim ownership of the original broadcast videos.
