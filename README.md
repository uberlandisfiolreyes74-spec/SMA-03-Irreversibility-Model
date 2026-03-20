# 🛠️ SMA-03: Manual de Implementación y Diagnóstico

Este repositorio contiene la caja de herramientas completa para aplicar el **Modelo Socio-Cognitivo SMA-03** a decisiones organizacionales críticas. Siga estas instrucciones para transformar datos cualitativos en una métrica cuantitativa de irreversibilidad.

## 📦 Contenido del Toolkit
1. **Paper Científico (`/docs`):** Fundamentación matemática y validación de casos (NVIDIA, Boeing, etc.).
2. **Motor de Cálculo (`/src`):** Script de Python (`sma03_engine.py`) para procesamiento avanzado.
3. **Cuestionario Interactivo (`/tools`):** Archivo Excel/CSV para recolección de datos en campo.

---

## 🚦 Guía de Inicio Rápido

### Paso 1: Recolección de Datos
Utilice el archivo `SMA-03_CUESTIONARIO_INTERACTIVO.csv`. Responda a las 25 preguntas utilizando la escala de Likert (1-5):
* **Sección 1 (P):** Presiones Estructurales.
* **Sección 2 (A):** Sistemas de Creencias.
* **Sección 3 (B):** Predisposiciones Biológicas (Flexibilidad Cognitiva).
* **Sección 4 (N):** Dinámica de Adopción Colectiva.

### Paso 2: Cálculo del Índice de Irreversibilidad (II)
Si usa la hoja de cálculo, el resultado se generará automáticamente. Si desea mayor precisión, ejecute el motor en Python:

```python
# Ejemplo rápido de uso
from src.sma03_engine import SMA03Model

model = SMA03Model()
# Introduzca sus promedios obtenidos del cuestionario
score = model.calculate_ii(P=[4, 5, 3, 5], A=4.5, B=0.8, D_t=1.2)
print(f"Índice de Irreversibilidad: {score}")
