# Simulador de Selección Natural 🧬

Una simulación de selección natural inspirada en el video ["Simulating Natural Selection"](https://www.youtube.com/watch?v=0ZGbIKd0XrM) del canal Primer. Este proyecto implementa un ecosistema donde criaturas (blobs) buscan comida, consumen energía, pueden morir y desarrollar mutaciones que les otorgan ventajas evolutivas.

## 🎯 Características

- **Blobs evolutivos**: Criaturas que se mueven por un mapa 2D buscando comida
- **Sistema de energía**: Los blobs consumen energía al moverse y la recuperan al comer
- **Mutaciones**: Aparición aleatoria de blobs con mayor velocidad
- **Selección natural**: Supervivencia y reproducción basada en la aptitud
- **Ciclo día/noche**: Los blobs regresan a su hogar al final de cada día
- **GUI interactiva**: Visualización en tiempo real con controles de velocidad
- **Estadísticas**: Seguimiento de población, mutaciones y velocidad promedio

## 🚀 Ejecución

### Requisitos
- Python 3.8+
- tkinter (incluido en la mayoría de instalaciones de Python)
- En sistemas Linux: `sudo apt-get install python3-tk`

### Uso

1. **Simulación en modo texto**:
   ```python
   # Ejecutar las celdas del notebook hasta la simulación sin GUI
   manager = SimulationManager()
   history = manager.run(days=10)
   ```

2. **Simulación con GUI**:
   ```python
   # Ejecutar la última celda del notebook
   manager_gui = SimulationManagerWithGUI()
   gui = SimulationGUI(manager_gui)
   gui.run()
   ```

## 🎮 Controles de la GUI

- **Iniciar/Pausar**: Controla la ejecución de la simulación
- **Control de velocidad**: Deslizador para ajustar la velocidad de actualización (10-300ms)
- **Indicadores visuales**:
  - 🟢 Cuadrados verdes: Comida disponible
  - 🔵 Círculos azules: Blobs normales
  - 🟠 Círculos naranjas: Blobs con mutación de velocidad

## 📊 Parámetros de Simulación

```python
MAP_WIDTH = 100          # Ancho del mapa
MAP_HEIGHT = 100         # Alto del mapa
STEPS_PER_DAY = 200      # Pasos por día de simulación
INITIAL_BLOB_COUNT = 20  # Población inicial
INITIAL_FOOD_COUNT = 40  # Comida por día
MUTATION_PROBABILITY = 0.2  # Probabilidad de mutación (20%)
```

## 🏗️ Arquitectura

### Clases Principales

1. **`Food`**: Representa unidades de comida en el mapa
   - Posición (x, y)
   - Valor energético
   - Estado de consumo

2. **`Blob`**: Las criaturas de la simulación
   - Posición y hogar
   - Energía y velocidad
   - Sistema de mutaciones
   - Comportamiento de búsqueda de comida

3. **`SimulationManager`**: Agente gestor del ecosistema
   - Manejo de población
   - Ciclo día/noche
   - Selección natural y reproducción
   - Generación de comida

4. **`SimulationGUI`**: Interfaz gráfica
   - Visualización en tiempo real
   - Controles de usuario
   - Estadísticas en pantalla

## 📈 Evolución Observable

A lo largo de la simulación puedes observar:

- **Supervivencia del más apto**: Blobs lentos tienden a morir más
- **Propagación de mutaciones**: Blobs rápidos se reproducen más
- **Fluctuaciones poblacionales**: La población se adapta a la disponibilidad de recursos
- **Convergencia evolutiva**: Aumento gradual de la velocidad promedio

## 🎓 Contexto Académico

Este proyecto fue desarrollado para la **Tercera Práctica Calificada** del curso **Tópicos en Ciencias de Computación**. Implementa conceptos de:

- Simulación multiagente
- Algoritmos evolutivos
- Sistemas complejos
- Interfaces gráficas de usuario
- Programación orientada a objetos

## 🤖 Declaración de IA

Durante el desarrollo se utilizó **GitHub Copilot** como asistente de programación para:
- Optimización de la interfaz gráfica
- Mejoras en el sistema de colores y visualización
- Refinamiento de la documentación
- Resolución de problemas técnicos con tkinter

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👨‍💻 Autor

Desarrollado como parte del curso de Tópicos en Ciencias de Computación.

---

*Inspirado en el fascinante mundo de la evolución y la selección natural* 🌱
# natural-selection-simulator
