# Puzzle 8 — Búsqueda Heurística

Implementación en Python del clásico Puzzle 8 con interfaz gráfica interactiva,
desarrollada como proyecto académico para la materia de Inteligencia Artificial.

## Descripción

El Puzzle 8 es un juego de deslizamiento sobre una cuadrícula 3×3 con 8 fichas
numeradas y un espacio vacío. El objetivo es mover las fichas desde una
configuración inicial hasta una configuración objetivo usando la menor cantidad
de movimientos posible.

Este proyecto resuelve el problema implementando **5 métodos de búsqueda**,
cada uno con su propia estrategia y características de rendimiento, visualizados
a través de una interfaz gráfica construida con Gradio sobre Google Colab.

---

## Métodos de búsqueda implementados

| Método | Tipo | Heurística |
|--------|------|------------|
| Primero en Amplitud (BFS) | No informado | ✗ |
| Primero en Profundidad (DFS) | No informado | ✗ |
| Ascenso en Colina | Informado | Distancia Manhattan |
| A* | Informado | Distancia Manhattan |
| Algoritmo Genético | Evolutivo | Distancia Manhattan |

---

## Características

- **Entrada por archivo de texto** — el estado inicial y el estado objetivo
  se cargan desde archivos `.txt` con formato de matriz 3×3
- **Verificación de solucionabilidad** — detecta automáticamente si una
  configuración es matemáticamente irresoluble antes de ejecutar la búsqueda
- **Visualización de estados** — muestra la secuencia completa de tableros
  desde el estado inicial hasta el estado final con colores por pieza
- **Secuencia de movimientos** — lista paso a paso cada movimiento realizado
- **Estadísticas por método** — nodos generados, nodos visitados y profundidad
  de la solución
- **Parámetros configurables** para el Algoritmo Genético: tamaño de población,
  longitud del cromosoma y tasa de mutación

---

## Cómo ejecutar

1. Abrir el notebook en Google Colab
2. Ejecutar todas las celdas en orden
3. Preparar un archivo `.txt` con el estado inicial en el siguiente formato:
```
1 2 3
4 5 6
7 0 8
```

> El `0` representa el espacio vacío del puzzle.

4. Subir el archivo en la interfaz, seleccionar el método de búsqueda y
   presionar **▶ Resolver**

---

## Estructura del proyecto
```
├── Puzzle_8.ipynb       # Notebook principal con todo el código
└── README.md
```

---

## Tecnologías

- **Python 3** — lenguaje de implementación
- **Gradio 6.x** — interfaz gráfica web
- **Google Colab** — entorno de ejecución
- `heapq` — cola de prioridad para A*
- `collections.deque` — cola para BFS
- `copy` — manejo de estados del puzzle
- `random` — generación de población y operadores genéticos

---

## Documentación UML

El proyecto incluye 7 diagramas UML:

- **1 diagrama de clases** — estructura de `Estadopuzzle` y relaciones
- **1 diagrama de estados** — ciclo de vida del sistema desde idle hasta solución
- **5 diagramas de secuencia** — uno por cada método de búsqueda

---

## Autores

- **Alejandro Alba Malagón**
- **David Santiago Mahecha Cruz**

---

## Licencia

Proyecto académico — Universidad. Todos los derechos reservados.
