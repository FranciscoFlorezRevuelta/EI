# 1. Example Based on the PsyMo Dataset

**Example Context**  
- **Trait**: Self-Esteem (Rosenberg Self-Esteem), with 3 ordinal classes: *Low*, *Normal*, and *High*.  
- **Subject**: ID 260 (part of the evaluation set, IDs 251–312).  
- **Runs considered**: 7 walks (one per variation, from a single camera angle) for simplicity.  
- **Variations**:  
  - `bg` → _Carry Bag_  
  - `cl` → _Clothing Change_  
  - `nm` → _Normal Walking_  
  - `ph` → _Talking on Phone_  
  - `txt` → _Texting_  
  - `wsf` → _Walk Speed Fast_  
  - `wss` → _Walk Speed Slow_  

## 1. Run-Level Evaluation  
Each of the 7 sequences is evaluated independently:

| Run | True Label | Model Prediction |
|-----|------------|------------------|
| 1   | High       | High             |
| 2   | Normal     | Normal           |
| 3   | High       | High             |
| 4   | High       | High             |
| 5   | Low        | Normal           |
| 6   | High       | High             |
| 7   | Low        | Low              |

- **True Positives (TP)** for the *High* class: 4  
- **False Positives (FP)** for *High*: 0  
- **False Negatives (FN)** for *High*: 0  
- **True Negatives (TN)** for *High*: 2  

Hence:  
$$
\text{Precision}_{\mathrm{High}} = \frac{4}{4+0} = 1.0,
\quad
\text{Recall}_{\mathrm{High}} = \frac{4}{4+0} = 1.0.
$$

And the **overall run-level accuracy** (7 runs, 6 correct):

$$
\text{Accuracy} = \frac{6}{7} \approx 86\%.
$$

## 2. Subject-Level Evaluation  
The 7 predictions are aggregated and a single label is assigned by majority vote:

| Prediction Count | High | Normal | Low |
|------------------|:----:|:------:|:---:|
| Times            | 4    | 2      | 1   |

- The majority class is **High** → final label for the subject.  
- Compared to the subject’s true label (High) → correct.

---

# 2. Meaning of the Label `000_00_0_0_bg`

The label follows the scheme: **SubjectID_SequenceIndex_CameraView_RunIndex_Variation**:

1. **`000` → Subject ID**  
2. **`00` → Sequence index** (first sequence).  
3. **`0` → Camera viewpoint** (0° frontal).  
4. **`0` → Run (repetition) index** (first pass).  
5. **`bg` → Variation code** (“carry bag”).

Altogether, `000_00_0_0_bg` is the file for the first sequence recorded with the front-facing camera (0°) on the first pass for subject 0, performing the “carry bag” variation.  
