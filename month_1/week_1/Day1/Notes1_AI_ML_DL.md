# Day 1 - What Is AI, ML, DL?
AI => Artificial Intelligence => Technology that makes computers act intelligently: Reasoning, problem-solving, perception...
Examples:
- Chess program that plans moves.
- Chatbot that answers questions.
- A self-driving car that makes decisions.

**AI** is the broad field: Any system that behaves "smartly," even if rule-based.

---

**ML** => Machine Learning => Let computers learn from examples, not rules.

Example:

**Classical rules**:
```python
if hours_studied > 5:
    grade = "A"
elif hours_studied > 3:
    grade = "B"
else:
    grade = "C"
```

**ML (The computer learns the rules on its own):**
| hours_studied | grade |
| ------------- | ----- |
| 1             | D     |
| 2             | C     |
| 4             | A     |
| 5             | B     |
| ...           | ...   |

ML = Learning patterns from data.

---

**DL** => Deep Learning => Use neural networks to learn complex patterns automatically, where ML needs features to be defined (like hours studied), DL can find its own patterns (from pixels, sounds or text...).
DL is a subset of ML, which is a subset of AI.

Examples:
- Detecting faces from raw images.
- Translating languages.
- Voice recognition.

**The core idea of learning:**
1. Input (X)  -> Example data (like numbers of study hours).
1. Output (Y) -> The target (like the final grade).
1. Model      -> A function that learns to map X to Y.

---

**Analogy: Chef and cooking**
| Step | AI analogy |
| ---- | ---------- |
| Read recipes | Collect data |
| Try cooking | Train the model |
| Taste and adjust | Compute loss and optimize |
| Improve next time | Model learn and reduces error |

NB: The code in this folder has an example of  basic grade calculation (Day1_1_grades_examples.ipyb)

-> The model test many "rules" (slopes).

-> It measures how far off each rule is (error).

This is what ML does, but with the smallest error.
