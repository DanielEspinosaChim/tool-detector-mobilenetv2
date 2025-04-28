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

- **Train Accuracy:** 94.4%
- **Test Accuracy:** 83.0%
- **Train Loss:** 0.169
- **Test Loss:** 0.644

### Matriz de Confusión
![Confusion Matrix](./ruta/del/confusion_matrix.png)

### Métricas por Clase (Test Set)
| Clase                | Precisión | Recall | F1-Score | Soporte |
|----------------------|-----------|--------|----------|---------|
| Alicates             | 0.90      | 0.92   | 0.91     | 92      |
| Leds                 | 0.76      | 0.90   | 0.82     | 49      |
| Arduino Mega         | 0.79      | 0.83   | 0.81     | 59      |
| Arduino Nano         | 0.74      | 0.95   | 0.83     | 80      |
| Arduino Uno          | 0.94      | 0.77   | 0.85     | 65      |
| Capacitores          | 0.80      | 0.82   | 0.81     | 60      |
| Destornilladores     | 0.73      | 0.78   | 0.76     | 60      |
| Diodos               | 0.91      | 0.70   | 0.79     | 43      |
| Jumpers              | 0.96      | 0.93   | 0.95     | 56      |
| Llaves Fijas         | 0.97      | 0.96   | 0.97     | 73      |
| Martillos            | 0.87      | 0.80   | 0.83     | 66      |
| Multímetros          | 0.92      | 0.97   | 0.94     | 69      |
| Pinzas               | 0.85      | 0.85   | 0.85     | 67      |
| Pistola de Silicón   | 0.83      | 0.78   | 0.80     | 55      |
| Potenciómetros       | 0.83      | 0.42   | 0.56     | 59      |
| Protoboards          | 0.78      | 0.88   | 0.82     | 48      |
| Raspberry Pi 3       | 0.86      | 0.73   | 0.79     | 60      |
| Raspberry Pi 4       | 0.80      | 0.85   | 0.83     | 62      |
| Raspberry Pi Pico    | 0.88      | 0.88   | 0.88     | 8       |
| Resistencias         | 0.65      | 0.70   | 0.67     | 44      |
| Soldadores           | 0.74      | 0.77   | 0.75     | 60      |
| Taladros             | 0.92      | 0.91   | 0.92     | 66      |
| Transistores         | 0.77      | 0.89   | 0.83     | 64      |

**Macro Average:**
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

