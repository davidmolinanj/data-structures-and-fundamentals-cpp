# Formal Algebraic Specifications in Maude

[![Language: Maude](https://img.shields.io/badge/Language-Maude-blue.svg)](http://maude.cs.illinois.edu/)
[![Topic: Formal Methods](https://img.shields.io/badge/Topic-Formal%20Methods-success.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey.svg)](#)

Este repositorio contiene especificaciones algebraicas formales y tipos abstractos de datos (TADs) desarrollados en el lenguaje de reescritura **Maude**, implementados bajo paradigmas funcionales puros y principios de deducción ecuacional.

---

## 📁 Estructura del Proyecto

* **`vocal.maude`**: Especificación ecuacional para el tipo elemental vocal (`V`) junto con predicados de comparación e igualdad estricta.
* **`natural.maude`**: Implementación de la aritmética de Peano para números naturales (`N`) que incluye suma, producto, relaciones de orden (`<`, `<=`) y control de subtipos de error (`NoN`).
* **`pila.maude`**: TAD Pila (LIFO) con operaciones de consulta profunda, conteo condicional de elementos y verificación estructural de igualdad.
* **`cola.maude`**: TAD Cola (FIFO) implementado con deducción recursiva sin heurísticas dependientes de orden (`[owise]`), con extensiones paramétricas basadas en naturales (`meterVarias`, `sacarVarias`).
* **`conjunto.maude`**: TAD Conjunto de elementos no duplicados con operaciones de teoría de conjuntos: unión, intersección, diferencia, relaciones de inclusión estricta (`⊂`), orden parcial (`⊆`) y detección de conjuntos disjuntos.

---

## 🛠️ Tecnologías y Conceptos

* **Lógica Ecuacional:** Módulos funcionales (`fmod ... endfm`).
* **Sistemas de Reescritura:** Reglas de reducción canónica sin bucles infinitos y verificables por confluencia y terminación.
* **Tipos Abstractos de Datos:** Separación estricta entre constructor primario, modificador y observador.
* **Aritmética Formal:** Aritmética inductiva mediante constructores `cero` y `sucesor`.

---

## 🚀 Ejecución y Verificación

Para cargar y probar cualquiera de las especificaciones en el entorno de Maude:

1. Iniciar Maude en la terminal:
   ```bash
   maude