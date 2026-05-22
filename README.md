# Sistema Visual Dinámico e Interactividad Paramétrica: Estudio Gráfico Basado en el Ukiyo-e

## 👤 Información del Proyecto
* **Nombre del Proyecto:** AFICHE DINÁMICO JAPONES 
* **Autor/a:** [Joan Esteven Acevedo Hernandez]
* **Institución:** Universidad Diego Portales
* **Facultad:** Facultad de Arquitectura, Arte y Diseño (FAAD)
* **Escuela:** Diseño
* **Asignatura:** Pensamiento Computacional
* **Evaluación:** Solemne II — Sistema visual dinámico e interactivo en p5.js

---

## 📝 Descripción Objetiva

### ¿Qué es el proyecto?
El proyecto consiste en el desarrollo de un sistema visual dinámico, reactivo e interactivo implementado en el entorno de programación creativa p5.js. El software está diseñado para procesar flujos de datos de entrada continuos provenientes del usuario, transformándolos en tiempo real en outputs formales variables regulados por una estructura algorítmica de bucles y condicionales lógicos.

### ¿Qué se ve en pantalla y qué elementos visuales aparecen?
El ciclo visual del lienzo se segmenta en dos estados de ejecución controlados por variables de estado lógico:
1. **Interfaz de Instrucciones (Estado Inicial):** Una pantalla de bienvenida estática compuesta por tres bloques de texto informativos ordenados de forma simétrica mediante coordenadas cartesianas explícitas, complementados por un botón de activación rectangular centralizado que despliega el rótulo `"PRESIONA AQUI PARA INICIAR"`.
2. **Lienzo Interactivo (Estado Activo):** Al conmutar el estado del programa, se despliega una grilla ortogonal bidimensional compuesta por la repetición modular de primitivas vectoriales (segmentos de recta verticales y círculos concéntricos). En el baricentro del lienzo se sitúa un núcleo tipográfico en formato de alta densidad estructural (*Bold*) que proyecta de forma variable las cadenas de texto `"TOKYO"` o `"ZEN"`.

### ¿Qué inputs utiliza y qué outputs genera?
* **Inputs del Sistema:** Captura posicional continua del cursor en el plano cartesiano (`mouseX` y `mouseY`), eventos discretos de presión del periférico de entrada (`mouseIsPressed`) y un acumulador temporal incremental global (`tiempo`).
* **Outputs del Sistema:** Modificación paramétrica del diámetro y el espesor de las líneas de la trama modular, alteración del tamaño del cuerpo tipográfico central, variación cromática de los vectores y distorsión de coordenadas cartesianas fijas mediante un algoritmo de ruido Perlin.

---

## 🎨 Descripción Conceptual

### Idea central del proyecto
La propuesta examina la tensión dialéctica entre la rigidez de las estructuras ortogonales calculadas y la mutabilidad orgánica de los fenómenos naturales. El sistema se comporta como un organismo visual sensible que transita desde un orden matemático predecible hacia una fluctuación caótica fluida, gatillada exclusivamente por la interacción del usuario.

### Corriente o referente de diseño con el que dialoga
El proyecto establece un diálogo conceptual y formal con la corriente artística del **Ukiyo-e** (grabados japoneses tradicionales del "mundo flotante"). Específicamente, se toma como eje de análisis la composición estructural del paisaje de la estampa tradicional japonesa del Monte Fuji. 

La traducción computacional no apela a una mímesis pictórica o copia estética superficial, sino a la transposición de sus leyes de composición subyacentes:
* El uso del espacio negativo o vacío pictórico (filosofía del espacio *Ma* o vacuidad Zen).
* La textura y el ritmo repetitivo lineal para la representación del viento y el agua ondulante.
* La superposición jerárquica de planos cromáticos lisos y bien delimitados.

### Principio de diseño explorado
Se explora el principio de **Ritmo y Variación en Sistemas Paramétricos**. A través de estructuras de control iterativas, el código establece un patrón visual isótropo y constante. No obstante, el sistema introduce de forma controlada factores de perturbación posicional y variaciones tipográficas continuas, demostrando cómo una regla matemática rígida puede albergar un comportamiento fluido y orgánico bajo un paradigma generativo.

---

## ⚙️ Input/Output y Sistema

### Reglas que gobiernan el sistema
El entorno gráfico se encuentra regido por una matriz de comportamiento lógicos basada en la posición y el estado del cursor:
1. **Modulación Métrica (Eje X):** La variable `mouseX` se procesa mediante una interpolación lineal para alterar de manera proporcional el diámetro de los círculos en la trama y la escala de la tipografía.
2. **Modulación Estructural (Eje Y):** La variable `mouseY` regula dinámicamente el valor del atributo `strokeWeight` en los segmentos lineales verticales.
3. **Activación de Umbral Izquierdo (Modo ZEN):** Al verificar que `mouseX < 50`, el sistema suspende los bucles de la trama de fondo e instrumenta una conmutación de cadena textual hacia `"ZEN"`, forzando la primacía del espacio negativo.
4. **Activación de Umbral Derecho (Perturbación Fluida):** Al verificar que `mouseX > width - 50`, el software rompe la rigidez de la cuadrícula cartesiana. Las variables de posición (`x`, `y`) son perturbadas mediante el mapeo de campos vectoriales basados en la función de ruido Perlin (`noise`), coordinada con la variable acumulativa `tiempo`.
5. **Inundación Cromática Discreta:** El condicional de entrada `mouseIsPressed` interrumpe la paleta por defecto para forzar la transición tonal inmediata de la trama hacia tonalidades de acento rosadas.

### Explicación del sistema de interactividad
* **Entrada (Input):** Monitoreo continuo de las coordenadas numéricas de la interfaz física del mouse en rangos de píxeles finitos.
* **Procesamiento:** Transformación matemática de los datos crudos del cursor mediante la función de mapeo paramétrico `map()`, traduciendo rangos espaciales a magnitudes de control formal (ej. escala de fuentes restringida entre un rango de 80pt y 220pt).
* **Salida (Output):** Redibujado del lienzo a una tasa estándar de 60 fotogramas por segundo, aplicando las propiedades computadas a las primitivas, garantizando una retroalimentación visual reactiva inmediata.

---

## 📊 Diagrama de Flujo del Sistema

El comportamiento de la arquitectura de software y el flujo de ejecución jerárquico del sketch se describen a través del siguiente mapa de procesos lógicos en texto:

[IMAGEN](<img width="1024" height="1536" alt="Diagrama_de_flujo png" src="https://github.com/user-attachments/assets/39894fd3-7c13-4716-bccf-d5fb17ce0f2a" /><img width="1024" height="1536" alt="Diagrama_de_flujo png" src="https://github.com/user-attachments/assets/158ad1e8-0db1-43c2-b180-adeab6e15348" />)
[IMAGEN][diagrama_flujo_tokyo_zen.pdf](https://github.com/user-attachments/files/28161211/diagrama_flujo_tokyo_zen.pdf)

##Enlaces del Proyecto
* **Sketch Ejecutable (Pantalla Completa):** [(https://editor.p5js.org/joan.acevedo/full/3a3sU4kKB)]
* **Código Fuente Editable (Editor p5.js):** [(https://editor.p5js.org/joan.acevedo/sketches/3a3sU4kKB)]


