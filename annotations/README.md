# Prosodic Phrase Annotated Dataset for Children

This dataset contains prosodic phrase annotations for children's reading materials, designed to identify natural pause locations for read-aloud scenarios.

## Dataset Overview

- **Total Stories**: 54 stories
- **Grade Range**: Grade 3 to Grade 8 
- **Stories per Grade**: 9 stories each (6 grades × 9 stories = 54 total)
- **Batches**: 3 CSV files, each containing 18 stories (3 stories from each grade)
- **Annotators**: 7 annotators per batch and per story (21 total annotators)
- **Target Audience**: Children aged 8-13

## Data Source

The stories are sourced from the **English 400 Reading Programme** by the Department of Materials Production, Central Institute of English and Foreign Languages (CIEFL). The programme uses a carefully researched vocabulary list prepared by language learning experts.

**Original Source**: https://www.orientblackswan.com/books?id=0&pid=0&sid=40

## File Structure

The dataset is divided into three batches:
- `annotations/Masked Dataset - Batch 1.csv` - 18 stories (3 from each grade)
- `annotations/Masked Dataset - Batch 2.csv` - 18 stories (3 from each grade) 
- `annotations/Masked Dataset - Batch 3.csv` - 18 stories (3 from each grade)

## Data Format

Each CSV file contains the following columns:

| Column | Description |
|--------|-------------|
| `Mask` | Semantically masked word |
| `StoryID` | Unique identifier for the story |
| `TokenID` | Individual word/token in the story |
| `R1` through `R7` | Individual annotator markings |
| `GT` | Agreement score across annotators |
| `GT_isboundary` | Presence of prosodic boundary (GT>=5) |
| `GT_boundary_forbidden` | Presence of forbidden pause (GT=0) |

### Annotation Schema

- **0**: No pause (continue reading)
- **1**: Pause (end of prosodic phrase)

### Example Data Rows

| Mask | StoryID | TokenID | R1 | R2 | R3 | R4 | R5 | R6 | R7 | GT | GT_isboundary | GT_boundary_forbidden |
|------|---------|---------|----|----|----|----|----|----|----|----|---------------|-----------------------|
| The  | G3S1 | G3010001 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |
| <entity_bird> | G3S1 | G3010002 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 2 | 0 | 1 |
| has | G3S1 | G3010003 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |
| <adjective_look>  | G3S1 | G3010004 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |
| feathers.  | G3S1 | G3010005 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 7 | 1 | 0 |

## Annotation Guidelines

Annotators were instructed to mark pauses at locations where they would naturally pause when **reading aloud to children aged 8-13**. The annotations capture prosodic phrase boundaries that facilitate comprehension and natural speech rhythm in educational read-aloud contexts.

#### Preview of the Annotation Tool used: 

<img width="500" height="500" alt="Screenshot 2025-05-18 at 2 27 36 AM" src="https://github.com/user-attachments/assets/aa79852b-5947-4e99-91b5-3413fd591049" />
<img width="500" height="500" alt="Screenshot 2025-05-18 at 2 26 23 AM" src="https://github.com/user-attachments/assets/ff53f7b5-21e5-4cf4-b6d9-83931b4f9261" />
<img width="500" height="500" alt="Screenshot 2025-05-18 at 2 26 47 AM" src="https://github.com/user-attachments/assets/67a35f42-5fe9-44c5-803c-1d5ee7cc320b" />



## Data Privacy and Masking

**⚠️ Important Disclaimer**: The original words have been semantically masked using placeholder tokens (e.g., `<object>`, `<character>`, `<action>`). As a result:

- Word length features may not exactly match original text
- Syllable count features may not exactly match original text  
- Semantic relationships are preserved through consistent placeholder categories
- The dataset maintains prosodic structure while protecting original content

## Use Cases

This dataset is suitable for research in:
- Prosodic phrase boundary prediction
- Text-to-speech systems for educational content
- Reading comprehension tools
- Child-oriented speech synthesis
- Educational technology applications

## Citation

If you use this dataset in your research, please cite:

```bibtex
@dataset{prosodic_phase_annotation_for_children_2025,
  title={Prosodic Boundary Prediction Children Texts},
  author={Mansi Dhamne, Sneha Raman, Preeti Rao},
  year={2025},
  note={Based on English 400 Reading Programme by CIEFL},
  url={https://github.com/mansidhamne/Prosodic-Boundary-Prediction-Children-Texts}
}
@inproceedings{
  dhamne2025predicting,
  title={Predicting Prosodic Boundaries for Children{\textquoteright}s Texts},
  author={Mansi Dhamne and Sneha Raman and Preeti Rao},
  booktitle={The 2025 Conference on Empirical Methods in Natural Language Processing},
  year={2025}
}
```

## Contact

For questions about this dataset, please contact: [mansiadhamne@gmail.com]

---

**Acknowledgments**: We thank the Central Institute of English and Foreign Languages (CIEFL) for developing the original English 400 Reading Programme materials that form the basis of this annotation dataset.
