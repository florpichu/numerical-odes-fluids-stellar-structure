
# Integradores numéricos desde cero: cinemática de fluidos y estructura estelar

Trabajo de la materia **Física de Fluidos** (FCEyN, UBA, 2024), realizado en conjunto con [Maximiliano Rodríguez Camps](https://github.com/).

Dos problemas de física resueltos mediante la implementación propia (sin librerías de integración numérica) de métodos de Runge-Kutta.

## Parte 1: Cinemática de campos de velocidad (RK2)

Implementación de un integrador **Runge-Kutta de orden 2** para calcular trayectorias, líneas de corriente y líneas de traza de partículas en distintos campos de velocidad bidimensionales: corriente uniforme oscilante en el tiempo, combinaciones de fuente/sumidero lineal, y torbellinos con circulación constante. Se generaron animaciones para visualizar la evolución temporal de cada campo.

## Parte 2: Estructura de una estrella autogravitante (RK4)

A partir de la ecuación de Euler para un fluido en equilibrio hidrostático bajo autogravitación, y asumiendo una ecuación de estado politrópica, se deriva la **ecuación de Lane-Emden**:

```
θ'' + (2/ξ) θ' + θⁿ = 0
```

Se implementó un integrador **Runge-Kutta de orden 4** para resolver esta ecuación diferencial no lineal —incluyendo el manejo de la singularidad matemática en el origen (ξ = 0)— para índices politrópicos n = 1 a 10, determinando para qué valores de n la estrella resultante tiene radio finito, y calculando el perfil de masa asociado.

## Por qué este trabajo

Más allá del contexto físico específico, este proyecto muestra la implementación de algoritmos numéricos fundamentales desde los primeros principios (sin depender de `scipy.integrate`), el manejo de ecuaciones diferenciales no lineales con condiciones de borde singulares, y la exploración sistemática de un espacio de parámetros.

## Herramientas

Python · NumPy · Matplotlib (incluye animaciones)
