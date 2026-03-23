# ✍️ Bitácora de Proyecto: Animación 2D con Grease Pencil en Blender

Este repositorio documenta el flujo de trabajo técnico y creativo para la creación de una secuencia de animación de 6 poses, integrando herramientas de dibujo 2D en un entorno 3D.

---

## 🏗️ 1. Configuración del Entorno de Trabajo

El proyecto inició con la preparación de un lienzo limpio optimizado para animación 2D.

* **Lienzo:** Se seleccionó el preset de **2D Animation** en Blender.
* **Composición de Área:** Se ajustó la vista de la cámara y se organizaron los paneles de la línea de tiempo (Dope Sheet) y propiedades de capas.

### 🎨 Gestión de Capas y Materiales
Para mantener un flujo no destructivo, se separó el arte en dos canales:
1. **Capa `Lines`:** Dedicada exclusivamente al trazo negro y contornos.
2. **Capa `Fills`:** Ubicada debajo de las líneas para el coloreado masivo.

**Materiales configurados:**
* `Stroke_Black`: Estilo sólido para el delineado.
* `Fill_Red_Light`: Color base para el cuerpo del personaje.
* `Fill_Red_Dark`: Tono de contraste para profundidad/sombra.

> **📸 CAPTURA DE PANTALLA 1:** *Muestra aquí tu panel de capas (Layers) y los slots de materiales.*
> ![Panel de capas y materiales](Ruta_a_tu_imagen_1.png)

---

## 🎬 2. Desarrollo de la Secuencia (Keyframing)

### Importación de Referencia
Se integró una **Image Reference** como guía visual para asegurar que las proporciones y la dinámica del movimiento fueran coherentes con la secuencia asignada en Classroom.

### Metodología de Animación
* **Cantidad de Poses:** 6 dibujos clave.
* **Timing:** Se estableció un intervalo de **6 fotogramas** entre cada pose para generar un ritmo pausado y claro.
* **Proceso de Dibujo:** Se utilizó la herramienta *Draw* con estabilización de trazo para definir las siluetas.

> **📸 CAPTURA DE PANTALLA 2:** *Muestra tu área de trabajo con la imagen de referencia al lado de tu dibujo.*
> ![Referencia y dibujo](Ruta_a_tu_imagen_2.png)

---

## 🛠️ 3. Control de Errores y Depuración Técnica

Durante la producción surgieron desafíos técnicos que requirieron el uso de herramientas avanzadas de edición:

1. **Problema de Fotogramas Duplicados:** Se detectaron múltiples dibujos ocupando el mismo espacio temporal en el fotograma 1.
   * **Solución:** Se utilizó el **Modo Edición** para aislar los trazos redundantes y eliminarlos (`X > Strokes`), dejando una sola pose limpia por cada 6 fotogramas.
2. **Alineación Espacial:** Para evitar saltos bruscos ("jittering"), se alineó la primera pose al origen y se ajustaron las siguientes basándose en el centro de masa del personaje.

> **📸 CAPTURA DE PANTALLA 3:** *Muestra la línea de tiempo (Dope Sheet) con los rombitos amarillos separados cada 6 espacios.*
> ![Timeline y Keyframes](Ruta_a_tu_imagen_3.png)

---

## 🚀 4. Resultados y Pulido Final

Tras completar los 6 dibujos, se realizó una prueba de reproducción (Playback). Se verificó que la transición entre poses fuera fluida y que los materiales (colores) estuvieran correctamente asignados a sus respectivos trazos.

### Resumen Técnico Final:
* **Motor de Render:** Eevee (Grease Pencil).
* **FPS de trabajo:** Ajustado para coincidir con el ritmo de la secuencia.
* **Técnica:** Animación pose a pose (Pose-to-Pose).

> **📸 CAPTURA DE PANTALLA FINAL:** *Muestra tu Kirby finalizado en el visor de Blender.*
> ![Resultado Final Kirby](Ruta_a_tu_imagen_4.png)

---
*Este proyecto fue desarrollado siguiendo las guías de Classroom y con asistencia de IA para la optimización del flujo de trabajo en Blender.*
