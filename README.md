# Laboratorio 5 - Reto Babel

Universidad del Valle de Guatemala, Deep Learning, semestre 2026.

El laboratorio entrena un traductor de un idioma inventado al español usando `nn.Transformer` de
PyTorch. Se parte de un diccionario de 22 palabras y 1200 frases paralelas de entrenamiento más 240
de validación. El idioma secreto ordena sujeto-objeto-verbo, pone el adjetivo antes del sustantivo y
la negación después del verbo, así que el modelo no solo traduce palabras, tiene que reordenarlas.
Además del traductor se hace una ablación que entrena la misma arquitectura sin codificación
posicional para medir cuánto pesa el orden.

## Cómo correr el proyecto

**1. Clonar el repositorio y entrar a la carpeta**

```bash
git clone https://github.com/GenserDev/Lab5-Deep.git && cd Lab5-Deep
```

**2. Crear un entorno virtual y activarlo**

```bash
python3 -m venv .venv && source .venv/bin/activate
```

**3. Instalar las dependencias**

```bash
pip install torch matplotlib jupyter
```

**4. Abrir el archivo principal**

```bash
jupyter notebook S09_Lab05_Reto_Babel_ESTUDIANTE.ipynb
```

**5. Ejecutar**

Reinicie el kernel y corra todas las celdas de arriba abajo.

Notas: los tres CSV ya están en `Datos/`, que es el valor de `CARPETA_DATOS`, así que el notebook se
debe abrir desde la raíz del repositorio. El notebook entrena dos modelos completos, con y sin
posición, y tarda unos minutos en CPU. Las celdas de verificación deben imprimir `OK`. En el Bloque 7
las frases son de prueba propias y hay que reemplazarlas por las que entregue el profesor.
