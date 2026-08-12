# Visualizador de Combinaciones Lineales en R³

Herramienta educativa interactiva para explorar el conjunto generado por un sistema de vectores en R³: **gen{ v₁, v₂, … }**.

## ¿Qué hace?

Dado un conjunto de vectores en R³, la herramienta:

- **Visualiza** el conjunto gen{ v₁, v₂, … } en un gráfico 3D interactivo:
  - **Dimensión 0** (solo el origen): un punto.
  - **Dimensión 1**: una recta que pasa por el origen.
  - **Dimensión 2**: un plano que pasa por el origen.
  - **Dimensión 3** (= R³): volumen verde semitransparente.
- **Muestra los ejes canónicos** x₁, x₂, x₃ como frame de referencia permanente.
- **Informa la dimensión** del conjunto generado en tiempo real.
- **Chequea pertenencia** de un vector de prueba **w**: determina si w ∈ gen{ v₁, … } y, si es así, devuelve los coeficientes de la combinación lineal explícita.

## Uso

Abrir `visualizador_gen.html` directamente en el navegador (no requiere servidor ni instalación).

### Vectores generadores

- Ingresá las tres componentes de cada vector en los campos de la barra lateral.
- Aceptan enteros, decimales (`0.2`) y fracciones (`3/10`).
- Usá **+ Agregar vector** para añadir más vectores y **×** para eliminar uno.
- El gráfico y la dimensión se actualizan automáticamente al tipear.

### Vector de prueba w

- Ingresá un vector **w** en los campos de la sección *Vector de prueba*.
- Presioná **¿Pertenece a gen{ }?** para verificar si w es combinación lineal de los generadores.
- Si pertenece, se muestran los coeficientes: `w = c₁·v₁ + c₂·v₂ + …`
- El resultado también se recalcula automáticamente cada vez que cambian los vectores generadores.
- Usá el checkbox para mostrar u ocultar **w** en el gráfico.

## Tecnologías

- HTML + CSS + JavaScript puro (sin frameworks).
- [Plotly.js](https://plotly.com/javascript/) para el gráfico 3D (cargado desde CDN).

## Contexto

Desarrollado para la materia **Métodos Computacionales** — UTDT.  
Pensado para introducir combinaciones lineales y conjuntos generados *antes* de formalizar el concepto de subespacio.
