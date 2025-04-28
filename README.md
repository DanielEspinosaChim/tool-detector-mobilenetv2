# Tool Detector with MobileNetV2

Este proyecto implementa un clasificador de herramientas usando Transfer Learning basado en MobileNetV2, con enfoque en precisión y optimización para dispositivos de recursos limitados.

## 📋 Descripción

Se utilizó la arquitectura **MobileNetV2** como **feature extractor** (preentrenada en ImageNet) y se añadió una capa de clasificación adaptada a 23 clases distintas de herramientas electrónicas y manuales.

**Algunas clases clasificadas:**
- Alicates
- Leds
- Arduino Uno, Mega, Nano
- Capacitores
- Destornilladores
- Martillos
- Multímetros
- Pistola de Silicón
- Soldadores
- Protoboards
- Raspberry Pi 3, 4 y Pico
- y más...

## 🧠 Modelo

- **Modelo base:** MobileNetV2 (`include_top=False`, `weights='imagenet'`)
- **Fine-Tuning:** Solo las capas finales son entrenadas
- **Entrenamiento:** 10 epochs con imágenes de tamaño 224x224 px
- **Framework:** TensorFlow/Keras

## 📈 Resultados de Evaluación

- **Train Accuracy:** 94.2%
- **Test Accuracy:** 83.9%
- **Train Loss:** 0.1775
- **Test Loss:** 0.6529

### Métricas por Clase (Test Set)

| Clase                | Precisión | Recall | F1-Score | Soporte |
|----------------------|-----------|--------|----------|---------|
| Alicates             | 0.84      | 0.89   | 0.86     | 92      |
| Leds                 | 0.77      | 0.84   | 0.80     | 49      |
| Arduino Mega         | 0.85      | 0.80   | 0.82     | 59      |
| Arduino Nano         | 0.76      | 0.94   | 0.84     | 80      |
| Arduino Uno          | 0.84      | 0.80   | 0.82     | 65      |
| Capacitores          | 0.74      | 0.75   | 0.74     | 60      |
| Destornilladores     | 0.81      | 0.83   | 0.82     | 60      |
| Diodos               | 0.83      | 0.67   | 0.74     | 43      |
| Jumpers              | 0.90      | 0.93   | 0.91     | 56      |
| Llaves Fijas         | 0.92      | 0.99   | 0.95     | 73      |
| Martillo             | 0.87      | 0.79   | 0.83     | 66      |
| Multímetro           | 0.97      | 0.93   | 0.95     | 69      |
| Pinzas               | 0.85      | 0.87   | 0.86     | 67      |
| Pistola de Silicón   | 0.87      | 0.82   | 0.84     | 55      |
| Potenciómetro        | 0.80      | 0.66   | 0.72     | 59      |
| Protoboards          | 0.96      | 0.94   | 0.95     | 48      |
| Raspberry Pi 3       | 0.74      | 0.82   | 0.78     | 60      |
| Raspberry Pi 4       | 0.81      | 0.71   | 0.76     | 62      |
| Raspberry Pi Pico    | 0.75      | 0.75   | 0.75     | 8       |
| Resistencias         | 0.78      | 0.73   | 0.75     | 44      |
| Soldadores           | 0.82      | 0.77   | 0.79     | 60      |
| Taladros             | 0.91      | 0.92   | 0.92     | 66      |
| Transistores         | 0.76      | 0.83   | 0.79     | 64      |

**Macro Average:**
- Precision: 0.83
- Recall: 0.82
- F1-Score: 0.83

**Weighted Average:**
- Precision: 0.84
- Recall: 0.83
- F1-Score: 0.83
## 🚀 Cómo usar

1. Clona el repositorio:
    ```bash
    git clone https://github.com/tu_usuario/tool-detector-mobilenetv2.git
    ```

2. Instala las dependencias:
    ```bash
    pip install tensorflow keras matplotlib scikit-learn
    ```

3. Entrena o prueba el modelo (`train.py` o `notebook.ipynb`).

4. Ajusta el modelo para nuevas clases modificando el dataset.

## 🛠️ Tecnologías usadas

- Python 3.11
- TensorFlow 2.x
- Keras
- Matplotlib
- scikit-learn

## 📄 Licencia

Este proyecto está bajo la licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

