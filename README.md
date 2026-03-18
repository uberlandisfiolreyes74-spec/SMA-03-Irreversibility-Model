Sociocognitive Model of Irreversibility

## Abstract

SMA-03 is a multilevel sociocognitive framework designed to model the probability of irreversibility in complex decision-making systems.

The model conceptualizes irreversibility as a probabilistic outcome emerging from the interaction between structural, behavioral, and sociocognitive variables.

---

## Theoretical Structure

SMA-03 integrates three dimensions:

### 1. Structural Dimension
- **P (Structural Pressure):** Institutional rigidity and systemic constraints  

### 2. Behavioral Dimension
- **A (Action Intensity):** Level of commitment and execution  

### 3. Sociocognitive Dimension
- **C (Causality Perception):** Interpretation of cause-effect relations  
- **I (Identity Involvement):** Degree of identity commitment  
- **S (Symbolic Reinforcement):** Narrative and symbolic consolidation  

---

## Core Model

The probability of non-reversibility (PNR) is defined as:
PNR = σ(β0 + β1P + β2A + β3C + β4I + β5S + β6(P·A) + β7(C·I) + β8(I·S))
Id="model_formula"
Copiar código
Where:

- **PNR:** Probability of Non-Reversibility  
- **σ:** Logistic (sigmoid) function  

---

## Implementation

This repository includes a Python implementation of the SMA-03 model.

### Example

```python
from model import SMA03Model

model = SMA03Model()

# Example input values (range 0–1)
P = 0.7
A = 0.6
C = 0.8
I = 0.9
S = 0.75

probability = model.predict_proba(P, A, C, I, S)
prediction = model.predict(P, A, C, I, S)

print(f"PNR: {probability:.4f}")
print("Irreversible" if prediction == 1 else "Reversible")
