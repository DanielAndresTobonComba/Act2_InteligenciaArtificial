# 🚀 Sistema de Optimización de Rutas con IA - washington

Un sistema inteligente para optimización de rutas de transporte agrícola en Washington, utilizando algoritmos clásicos e Inteligencia Artificial multi-objetivo.

## 📋 Descripción del Proyecto

Este sistema calcula rutas óptimas para el transporte de productos agrícolas considerando múltiples factores:
- **Red vial real** de washington y municipios aledaños
- **Factores externos**: tráfico, clima, obras, retenes
- **Múltiples objetivos**: distancia, tiempo, riesgo, calidad

## 🏗️ Estructura del Proyecto

```
proyecto_rutas_ia/
├── src/
│   ├── main.py                 # Punto de entrada principal
│   ├── menu.py                 # Controlador del sistema interactivo
│   ├── clases.py               # Modelos de datos (Nodo, AristaVial, FactoresExternos)
│   ├── redvial.py              # Descarga y gestión de red vial (OSMnx)
│   ├── integrador_nodos.py     # Gestión de nodos de producción
│   ├── calculador_rutas.py     # Algoritmos de cálculo de rutas
│   ├── factores_viales.py      # Gestión de factores externos
│   ├── ia_multiobjetivo.py     # Sistema de IA para predicciones
│   ├── extractor_caracteristicas.py # Extracción de features para IA
│   ├── comparador_algoritmos.py # Comparación de algoritmos
│   └── visualizador_red.py     # Visualización con mapas interactivos
├── requirements.txt            # Dependencias del proyecto
└── README.md                   # Este archivo
```

## 🚀 Instrucciones para ejecutar el proyecto

### 1️⃣ Crear el entorno virtual
```bash
python -m venv .venv
```

### 2️⃣ Activar el entorno virtual

#### 🔵 Linux / macOS
```bash
source .venv/bin/activate
```

#### 🟣 Windows (PowerShell)
```powershell
.\.venv\Scripts\activate
```

#### 🟠 Windows (CMD)
```cmd
.\.venv\Scripts\activate.bat
```

### 3️⃣ Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4️⃣ Ejecutar el proyecto
El archivo principal se encuentra dentro de la carpeta `src`.

```bash
python src/main.py
```

## 📦 Dependencias Principales

- **networkx**: Manipulación de grafos y redes
- **osmnx**: Descarga de datos de OpenStreetMap
- **folium**: Visualización de mapas interactivos
- **scikit-learn**: Algoritmos de machine learning
- **numpy**: Cálculos numéricos
- **matplotlib**: Gráficos y visualizaciones

## 🎯 Características Principales

### 🔍 Red Vial Real
- Descarga automática de calles de washington desde OpenStreetMap
- Miles de intersecciones y calles reales
- Información completa: distancias, velocidades, tiempos de viaje

### 🤖 IA Multi-Objetivo
- Predicción de distancia, tiempo y riesgo de rutas
- Entrenamiento con rutas reales calculadas
- Evaluación de calidad general de rutas

### 📊 Comparación de Algoritmos
- **Dijkstra**: Ruta más corta por tiempo
- **Bellman-Ford**: Manejo de pesos negativos
- **A***: Búsqueda heurística eficiente
- **IA**: Predicciones inteligentes

### 🗺️ Visualización Interactiva
- Mapas con Folium mostrando rutas reales
- Capas para diferentes tipos de nodos (parcelas, centros, plantas)
- Información detallada de cada ruta calculada

### 🌦️ Factores Externos
- Simulación de hora pico
- Condiciones climáticas adversas
- Retenes policiales y accidentes
- Obras viales

## 💡 Uso del Sistema

### Menú Principal
El sistema ofrece un menú interactivo con las siguientes opciones:

1. **Inicializar sistema**: Descarga la red vial de washington
2. **Calcular ruta específica**: Calcula y visualiza una ruta entre dos puntos


### Ejemplo de Uso

```python
# El sistema se controla mediante el menú interactivo
# Después de ejecutar python src/main.py:

# 1. Selecciona opción 1 para inicializar el sistema
# 2. Usa opción 3 para calcular rutas específicas

```

## 📈 Resultados y Métricas

El sistema proporciona:
- **Distancias** en kilómetros
- **Tiempos** de viaje en minutos
- **Tiempos de ejecución** de algoritmos
- **Evaluación de riesgo** (BAJO, MEDIO, ALTO)
- **Score de calidad** de rutas
- **Comparativas** entre algoritmos

## 🗂️ Tipos de Nodos

- **🌳 Parcelas agrícolas** (P001-P025): Fincas productoras
- **🏪 Centros de acopio** (C001-C006): Puntos de recolección
- **🏭 Plantas procesadoras** (PL001-PL004): Procesamiento final
- **🛒 Mercados** (M001-M004): Puntos de distribución

## 🔧 Configuración

### Parámetros Ajustables
- Número de escenarios para entrenamiento de IA
- Tipos de factores externos a simular
- Algoritmos a comparar
- Criterios de optimización (distancia, tiempo, riesgo)

## 📊 Salidas del Sistema

- **Mapas HTML** interactivos con rutas visualizadas
- **Gráficos comparativos** en PNG
- **Tablas de resultados** en consola
- **Modelos de IA** guardados para reutilización

## 🐛 Solución de Problemas

### Error de descarga de red vial
- Verificar conexión a internet
- Reintentar la descarga
- Usar red vial previamente guardada


### Visualización de mapas
- Verificar que se generen archivos HTML
- Abrir manualmente si el navegador no se abre automáticamente

## 📄 Licencia

Este proyecto es para fines educativos y de investigación.

---

**¡Listo para optimizar rutas en washington!** 🚀
