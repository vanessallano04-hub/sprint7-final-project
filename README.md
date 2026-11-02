# Análisis Exploratorio de Datos de Consumo y Usuarios

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es realizar un Análisis Exploratorio de Datos (EDA) sobre un conjunto de datos de usuarios de telecomunicaciones y sus patrones de consumo (llamadas y mensajes). A través de este análisis se busca identificar inconsistencias de datos, evaluar la distribución del consumo por plan y detectar anomalías o datos ausentes/sentinels para garantizar la calidad de los datos previa al modelado o toma de decisiones operativas.

---

## 📊 Datasets Utilizados
El análisis integra y evalúa los siguientes datos:
* **Datos de Usuarios**: Información demográfica y de registro (`user_id`, `age`, `city`, `plan`, `reg_date`).
* **Datos de Consumo de Servicios**: Registros de actividad telefónica y mensajería (`type`, `duration`, `length`, `id`).

---

## 🛠️ Etapas del Análisis Realizadas
1. **Inspección de Identificadores**: Verificación de rangos válidos e integridad en `user_id` e `id` (sin valores repetidos fuera del estándar).
2. **Evaluación Demográfica y Geográfica**:
   * Identificación del valor *sentinel* `-999` en la columna `age` para marcar datos faltantes.
   * Detección del carácter `'?'` en la columna `city` como marcador de ubicación desconocida.
3. **Validación de Servicios y Planes**:
   * Confirmación de categorías válidas en `plan` (`Basico`, `Premium`) y en `type` (`call`, `text`).
4. **Análisis de Consumo (`duration` y `length`)**: Revisión de promedios, máximos y valores en `0` (eventos sin consumo efectivo).
5. **Auditoría Temporal**: Identificación de inconsistencias en `reg_date` (registros marcados en 2026 frente a datos de consumo del período 2024).

---

## 🚀 Cómo Ejecutar el Notebook

### Opción 1: Google Colab (Recomendado)
1. Descarga el archivo `.ipynb` de este repositorio o accede desde el enlace de Google Colab.
2. Abre [Google Colab](https://colab.research.google.com/).
3. Haz clic en **Archivo > Subir cuaderno** y selecciona el archivo del proyecto.
4. Asegúrate de cargar los datasets correspondientes en el entorno de Colab.
5. Ejecuta las celdas en secuencia presionando `Shift + Enter` o desde **Entorno de ejecución > Ejecutar todas**.

### Opción 2: Jupyter Notebook local
1. Clona este repositorio en tu equipo:
   ```bash
   git clone [https://github.com/vanessallano04-hub/sprint7-final-project.git](https://gith
