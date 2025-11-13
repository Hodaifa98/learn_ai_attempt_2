# Day 2 - How machines see the world
Humans      => A student who obtained 3 hours got 70%.
A machine    => [3] -> [70]

Computers don't understand concepts, only numbers.

So every input (image, text, sound...) must be translated into numbers = representation.

### 1- Real life -> Numbers:
| Real concept | Machine representation |
| ------------ | ---------------------- |
| Hours studied | 3.0 |
| Has notes (yes/no) | 1 or 0 |
| Color (white/black) | 0 or 1 (or one-shot encoded |
| Image | Matrix of pixel values (0-255) |

-> Everything, even text and pictures, becomes a list or grid of numbers.

NB: *One-shot encoding:* Turns a categorical variable into a vector of 0s and 1s.

One position for each possible category, since there is no relationship between them (for example, colors could be something besides just black and white...)

So it's represented as White [1, 0] and Black [0, 1]

---

### 2- The two types of data in ML:
- **Feature (X)** -> The input fed to the model      => Ex: Final grade.
- **Label (Y)**   -> The answder / expected output   => Ex: Final grade.
We train the model with pairs (x, y) so it can learn a pattern.

(1 -> 50), (2 -> 60), (3 -> 65), (4 -> 70) => Then we can give it a new X (like 5 hours) and it'll predict the new Y.

---

### 3- Data shapes and dimensions:
ML models expect data in arrays (or tables).
```python
import numpy as np
# Each column = one feature.
# Each row = one example
X = np.array([
  [1, 0], # One hour, no note
  [2, 1], # Two hours, one note
  [3, 1],
  [4, 1]
])

Y = np.array([50, 60, 65, 70])

print("Shape of X:", X.shape)
print("Shape of Y", Y.shape)
```
**Output:** 

- Shape of X: (4, 2) => 4 examples
- Shape of Y: (4,)   => Each example has 2 features

---

# 4- Visualizing Features and Labels:
```python
import matplotlib.pyplot as plt
hours = X[:,0] # From every row in X, take the first column
grades = Y

plt.scatter(hours, grades, color="blue")
plt.title("Study hours vs Grades")
plt.xlabel("Hours studied")
plt.ylabel("Grade(%)")
plt.show()
```

- This code draws a **scatter plot**, where *x-axis* = hours studied and *y-axis* = grades. And blue dots represent each student data-point.
- We see a line-like pattern => that's what the model will try to learn.
- The better the data pattern, the easier it is for the AI to learn.

---

# 5- Grarbage in = garbage out:
AI is only as smart as its data. If the dataset has:
- Missing values
- Wrong labels
- Biased examples
Then the AI will learn those mistakes. That's why data cleaning is as important as the algorithm itself.
