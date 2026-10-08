# EV Colombia — Decision Model

Fecha: 2026-10-08

## 1. Objetivo

Definir cómo EV Colombia transforma información del usuario y datos externos en una recomendación contextual.

---

# 2. Inputs

## Persona

- ciudad;
- vivienda;
- posibilidad de carga;
- kilometraje;
- frecuencia de viajes;
- presupuesto.

## Vehículo

Cuando exista:

- precio;
- autonomía;
- consumo;
- batería;
- potencia de carga;
- conectores;
- características relevantes.

## Infraestructura

- estaciones;
- conectores;
- potencia;
- disponibilidad cuando exista;
- precio cuando exista;
- ubicación;
- distancia;
- confiabilidad cuando exista.

## Ruta

- origen;
- destino;
- distancia;
- estaciones disponibles;
- carga rápida;
- alternativas.

---

# 3. Dimensiones de decisión

El sistema debe evaluar:

### Charging Fit

¿Puede el usuario resolver la carga?

### Cost Fit

¿El vehículo encaja económicamente?

### Vehicle Fit

¿El vehículo corresponde al uso?

### Travel Fit

¿Los viajes habituales son razonablemente viables?

### Infrastructure Fit

¿Existe infraestructura adecuada para el perfil?

---

# 4. Resultado

Resultado conceptual:

EV REALITY SCORE

0–100

El resultado debe acompañarse de:

- explicación;
- fortalezas;
- riesgos;
- recomendaciones.

---

# 5. Ejemplo

EV Reality Score: 83/100

### Charging Fit

62/100

Problema principal:

El usuario no dispone de carga residencial.

### Cost Fit

91/100

El costo operativo puede ser favorable.

### Vehicle Fit

88/100

El vehículo corresponde al kilometraje indicado.

### Travel Fit

79/100

Los viajes habituales requieren planificación.

### Infrastructure Fit

86/100

La infraestructura disponible parece suficiente para el patrón analizado.

---

# 6. Regla de transparencia

Nunca mostrar solamente:

> 83/100

Debe existir una explicación:

> "Tu score es 83 porque tu uso urbano y kilometraje favorecen un EV, pero la ausencia de carga residencial reduce tu resultado."

---

# 7. Dealbreakers

El motor debe detectar condiciones que puedan cambiar significativamente la recomendación.

Ejemplos:

- imposibilidad de carga;
- presupuesto insuficiente;
- viajes incompatibles con autonomía;
- infraestructura insuficiente;
- vehículo incompatible con necesidades.

---

# 8. Resultado accionable

Cada diagnóstico debe terminar con una acción.

Ejemplos:

> Revisar vehículos compatibles.

> Calcular costo.

> Resolver carga residencial.

> Evaluar una ruta.

> Ver cargadores cercanos.

---

# 9. Estado

Este modelo es conceptual.

Los pesos y reglas deben validarse antes de convertirse en lógica definitiva de producción.
