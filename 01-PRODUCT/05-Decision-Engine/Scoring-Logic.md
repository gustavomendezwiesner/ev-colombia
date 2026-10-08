# EV Colombia — Scoring Logic

Fecha: 2026-10-08

## 1. Objetivo

Definir una primera estructura para calcular scores sin presentar los pesos como datos científicamente validados.

Los pesos iniciales son hipótesis de producto.

---

# 2. EV Reality Score

Componentes propuestos:

| Dimensión | Peso inicial |
|---|---:|
| Charging Fit | 30% |
| Cost Fit | 25% |
| Vehicle Fit | 20% |
| Travel Fit | 15% |
| Infrastructure Fit | 10% |

Total:

100%.

---

# 3. Charging Fit

Variables potenciales:

- posibilidad de cargar en casa;
- posibilidad de instalar cargador;
- distancia a infraestructura pública;
- disponibilidad de carga pública;
- compatibilidad.

La ausencia de carga residencial debe tener un impacto significativo, pero no necesariamente producir un NO automático.

---

# 4. Cost Fit

Variables potenciales:

- precio del vehículo;
- kilometraje mensual;
- costo de energía;
- costo de combustible equivalente;
- mantenimiento;
- otros costos relevantes.

Debe evitarse presentar ahorro exacto cuando los datos sean estimaciones.

---

# 5. Vehicle Fit

Variables potenciales:

- autonomía;
- kilometraje;
- uso urbano;
- uso carretera;
- presupuesto;
- velocidad de carga;
- compatibilidad de conectores.

---

# 6. Travel Fit

Variables potenciales:

- frecuencia de viajes;
- distancia;
- infraestructura disponible;
- necesidad de carga;
- carga rápida;
- alternativas.

---

# 7. Infrastructure Fit

Variables potenciales:

- cantidad de infraestructura relevante;
- distancia;
- conectores;
- potencia;
- disponibilidad;
- confiabilidad.

La calidad del dato debe considerarse.

---

# 8. Confidence

El score debería incorporar eventualmente una medida de confianza.

Ejemplo:

### Score

83/100

### Confidence

Alta

o:

### Confidence

Media

Esto evita presentar como certeza una recomendación basada en datos incompletos.

---

# 9. Regla de datos

Cada variable crítica debería mantener:

- source;
- source_timestamp;
- last_verified;
- confidence.

---

# 10. Interpretación

Ejemplo conceptual:

### 90–100

Excelente encaje.

### 75–89

Buen encaje.

### 60–74

Encaje posible con condiciones.

### 40–59

Existen riesgos importantes.

### 0–39

Probablemente no es adecuado actualmente.

Estos rangos son hipótesis de UX y deben validarse.

---

# 11. Regla fundamental

El score NO debe pretender decir:

> "Este es el mejor carro."

Debe responder:

> "Con la información disponible, este vehículo parece encajar así con tu situación."

---

# 12. Evolución

Los pesos podrán modificarse posteriormente usando:

- comportamiento;
- feedback;
- datos reales;
- resultados de usuarios;
- validación de expertos;
- desempeño predictivo.

No congelar esta lógica como definitiva en el MVP.
