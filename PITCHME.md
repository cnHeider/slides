---

Model

The archiecture:

7200-500-250-50-250-500-7200

relu-relu-relu-tanh-relu-relu-relu-linear

+++

```python
def encoding_layers(encoding_size):
  return [
    BatchNormalization(),
    Dropout(0.2),
    Dense(500, activation='relu'),

    BatchNormalization(),
    Dropout(0.2),
    Dense(250, activation='relu'),

    BatchNormalization(),
    Dropout(0.2),
    Dense(50, activation='relu'),

    Dense(encoding_size, activation='tanh')
  ]
```

+++

```python
def decoding_layers(input_size):
  return [
    BatchNormalization(),
    Dropout(0.2),
    Dense(50, activation='relu'),

    BatchNormalization(),
    Dropout(0.2),
    Dense(250, activation='relu'),

    BatchNormalization(),
    Dropout(0.2),
    Dense(500, activation='relu'),

    Dense(input_size, activation='linear')
  ]
```

---
The 50 principle components

+++

![pca1](3pca-model1.png)

+++

![pca2](3pca-model1-2.png)

+++

![pca3](3pca-model1-3.png)

+++

![pca4](3pca-model1-4.png)

---?gist=92814a9bfbe076e4613778165133538b

---
![r1](original-model-1.png)
+++
![r1](reconstruction-model-1.png)

---
![r2](original-model-1-2.png)
+++
![r2](reconstruction-model-1-2.png)

---
![r3](original-model-1-3.png)
+++
![r3](reconstruction-model-1-3.png)

---
![r4](original-model-1-4.png)
+++
![r4](reconstruction-model-1-4.png)

---
![r5](original-model-1-5.png)
+++
![r5](reconstruction-model-1-5.png)

---
![r6](original-model-1-6.png)
+++
![r6](reconstruction-model-1-6.png)

---

The End :)

---


```
function test() {
  console.log("notice the blank line before this function?");
}
```
