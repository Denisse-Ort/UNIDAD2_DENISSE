<img width="1366" height="279" alt="PROYECTO INTEGRADOR U2 (1)" src="https://github.com/user-attachments/assets/c3401915-ab53-44e6-b97f-1ce70f6c003e" />

# Investigación Extensa: Unidad 2 - Graficación 2D


## 2.1 Transformación Bidimensional

Las transformaciones bidimensionales son el núcleo de la computación gráfica. Se definen como aplicaciones matemáticas:

$$
f: \mathbb{R}^2 \to \mathbb{R}^2
$$

Estas transformaciones permiten modificar las propiedades espaciales de los objetos, como su posición, tamaño y orientación, siendo fundamentales en videojuegos, interfaces gráficas y simulaciones.



### 2.1.1 Traslación

La traslación es una transformación rígida que mueve un objeto sin alterar su forma ni su rotación.

Se basa en un vector de desplazamiento:

$$
\vec{T} = (t_x, t_y)
$$

Para un punto $P(x, y)$:

$$
x' = x + t_x
$$

$$
y' = y + t_y
$$

**Propiedades:**
Es una operación aditiva.
Dos traslaciones consecutivas se combinan:

$$
\vec{T}_{final} = \vec{T}_1 + \vec{T}_2
$$

---

### 2.1.2 Escalamiento

El escalamiento modifica el tamaño de un objeto multiplicando sus coordenadas por factores de escala:

$$
(s_x, s_y)
$$

**Tipos de escalamiento:**

**Uniforme:** $s_x = s_y$ → mantiene proporciones.
**No uniforme:** $s_x \neq s_y$ → distorsiona la figura.

**Punto fijo:**
Por defecto se realiza respecto al origen $(0,0)$. Para escalar respecto a un punto $(x_f, y_f)$:
1. Trasladar al origen
2. Escalar
3. Re-trasladar



### 2.1.3 Rotación

La rotación gira un objeto alrededor de un punto (generalmente el origen).

Ecuaciones:

$$
x' = x \cos \theta - y \sin \theta
$$

$$
y' = x \sin \theta + y \cos \theta
$$

- $\theta > 0$ → rotación antihoraria



### 2.1.4 Sesgado (Shearing)

El sesgado desplaza puntos en función de su distancia respecto a un eje.

**Sesgado en X:**

$$
x' = x + sh_x \cdot y
$$

$$
y' = y
$$

**Aplicaciones:**
 Simulación de perspectiva
 Sombras
 Tipografía cursiva

## 2.2 Representación Matricial de Transformaciones

Para optimizar cálculos se usan **coordenadas homogéneas**:

$$
(x, y, 1)
$$

### Matrices de Transformación

**Traslación:**

$$
M_T =
\begin{bmatrix}
1 & 0 & t_x \\
0 & 1 & t_y \\
0 & 0 & 1
\end{bmatrix}
$$

**Escalamiento:**

$$
M_S =
\begin{bmatrix}
s_x & 0 & 0 \\
0 & s_y & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Rotación:**

$$
M_R =
\begin{bmatrix}
\cos \theta & -\sin \theta & 0 \\
\sin \theta & \cos \theta & 0 \\
0 & 0 & 1
\end{bmatrix}
$$



### Concatenación de Transformaciones

Para aplicar múltiples transformaciones:

$$
M = T \cdot S \cdot R
$$

 **Importante:**  
El orden importa, ya que la multiplicación de matrices **no es conmutativa**.

---

### Implementación de Control

En sistemas interactivos (como teclado):
- Se mantiene una **matriz de estado**
- Cada acción multiplica la matriz actual por una nueva transformación



https://github.com/user-attachments/assets/697703a1-926d-4cd9-a2d1-9be3a80071bc



## 2.3 Trazo de Líneas Curvas

Las curvas se representan mediante funciones paramétricas.


### 2.3.1 Curvas de Bézier

Usadas en diseño vectorial (SVG, tipografías).

**Características:**
 Definidas por puntos de control
 Una curva de grado $n$ tiene $n+1$ puntos

**Algoritmo de Casteljau:**
 Realiza interpolaciones sucesivas
 Genera puntos para $t \in [0,1]$



### 2.3.2 B-Spline

Mejoran limitaciones de Bézier.

**Ventajas:**
 Grado independiente del número de puntos
 Control local (modifica solo una parte de la curva)

<img width="561" height="352" alt="image" src="https://github.com/user-attachments/assets/730c6e34-061b-4f6f-bc4d-fcc67dd2ec2e" />


## 2.4 Fractales

Un fractal es una estructura con complejidad infinita y autosimilitud.

**Concepto matemático:**
Dimensión de Hausdorff mayor que la topológica.



### Tipos de fractales

- **Sistemas de Funciones Iteradas (IFS):**
  - Ejemplo: Helecho de Barnsley

- **Atractores extraños:**
  - Representan sistemas dinámicos caóticos

- **Fractales de escape:**
  - Ejemplo: Conjunto de Julia



## 2.5 Uso y Creación de Fuentes de Texto

El renderizado de texto es complejo por la necesidad de precisión visual.



### Estructura de un glifo

 Representación visual de un carácter
 Definido mediante curvas de Bézier



### Proceso de creación

1. **Diseño de contorno**
    Definición vectorial de letras

2. **Hinting**
   Ajustes para mejorar legibilidad en baja resolución

3. **Rasterización**
   Conversión a píxeles
   Uso de *antialiasing*



## Referencias Bibliográficas (APA)

- Foley, J. D., Van Dam, A., Feiner, S. K., & Hughes, J. F. (2013). *Computer Graphics: Principles and Practice* (3rd ed.). Addison-Wesley Professional.
- Hearn, D., & Baker, M. P. (2011). *Computer Graphics with OpenGL* (4th ed.). Pearson.
- Mandelbrot, B. B. (1982). *The Fractal Geometry of Nature*. W. H. Freeman and Company.
- Rogers, D. F., & Adams, J. A. (1990). *Mathematical Elements for Computer Graphics*. McGraw-Hill.
- Salomon, D. (2006). *Curves and Surfaces for Computer Graphics*. Springer.
