# EV Colombia — SIEM / OCPI Research

Fecha: 2026-10-08

## 1. Hallazgo principal

El SIEM de la UPME cambia una hipótesis importante del proyecto.

La información de infraestructura de carga está avanzando hacia una arquitectura nacional estandarizada.

La Resolución 40559 de 2025 establece la obligación de los CPO públicos de reportar información al SIEM.

Fuente oficial:

https://www.upme.gov.co/simec/siem/

---

## 2. OCPI

Colombia adopta OCPI 2.2.1 como estándar de interoperabilidad.

El SIEM funciona como hub de interoperabilidad entre CPO y otros actores.

Esto permite estandarizar información como:

- ubicaciones;
- puntos de carga;
- conectores;
- disponibilidad;
- tarifas;
- sesiones.

---

## 3. API

La documentación técnica de UPME muestra endpoints OCPI bajo:

https://siem.upme.gov.co/ocpi/2.2.1/

La documentación también indica autenticación mediante Bearer/JWT para los endpoints de integración.

Por tanto:

NO asumir que EV Colombia puede consumir todo el SIEM anónimamente.

Debe investigarse:

- API pública;
- autenticación;
- módulos disponibles;
- permisos;
- rate limits;
- términos de uso;
- cobertura;
- frecuencia;
- licencia;
- disponibilidad de datos históricos.

Fuente técnica:

https://docs.upme.gov.co/Normatividad/Circular_047_2026_anexo.pdf

---

## 4. Implicación estratégica

La información bruta de estaciones puede convertirse en un commodity.

Por eso:

NO construir el moat únicamente alrededor de:

> "Tenemos una base de datos de cargadores."

---

## 5. Posible arquitectura de datos

FUENTES

↓

SIEM / OCPI

↓

Operadores

↓

Open Data

↓

OpenStreetMap

↓

Fuentes propias

↓

Normalización

↓

EV Colombia Data Layer

↓

Scores / recomendaciones / SEO

---

## 6. Datos propios potencialmente diferenciales

EV Colombia podría generar información que no sea simplemente infraestructura:

- EV Readiness;
- Vehicle Fit;
- City EV Score;
- Route Score;
- costo real;
- experiencia del usuario;
- confiabilidad histórica;
- tiempos;
- reportes;
- comportamiento;
- preferencias.

Esto podría constituir un activo de datos más interesante.

---

## 7. Riesgo

No diseñar la arquitectura suponiendo que una API específica estará siempre disponible.

Debe existir:

- fuente primaria;
- fuentes secundarias;
- actualización;
- timestamp;
- source;
- confidence score.

---

## 8. Modelo mínimo de calidad

Cada dato crítico debería poder tener:

`source`

`source_timestamp`

`last_verified`

`confidence`

`status`

Ejemplo:

Station

- source = SIEM
- last_verified = 2026-10-08
- confidence = high

---

## 9. Conclusión

SIEM puede reducir considerablemente la dificultad de construir una capa nacional de infraestructura.

Pero eso también reduce la posibilidad de que la infraestructura bruta sea el diferencial.

La oportunidad está en construir encima:

> datos + contexto + decisión + experiencia.

---

## Próxima investigación

Antes de implementar el ingestion layer:

1. confirmar acceso público;
2. documentar endpoints;
3. identificar módulos;
4. probar sandbox;
5. identificar campos;
6. revisar términos;
7. revisar frecuencia;
8. evaluar cobertura real.

No implementar integración productiva hasta completar esta validación.
