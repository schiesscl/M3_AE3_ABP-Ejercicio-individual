# M3_AE3_ABP-Ejercicio individual

## Hans Schiess

## 📋 Descripción del Proyecto

Este programa en Python implementa un sistema inteligente de cálculo de descuentos para compras, considerando múltiples criterios como cantidad de productos, historial del cliente, monto total y días de promoción especial.

## 🎯 Objetivo

Determinar automáticamente el descuento aplicable a una compra según criterios específicos, garantizando que ningún cliente obtenga un descuento superior al 30% del total.

## 📊 Criterios de Descuento

El sistema aplica descuentos acumulativos basados en las siguientes condiciones:

| Criterio | Condición | Descuento |
|----------|-----------|-----------|
| Cantidad de productos | ≥ 10 productos | 10% |
| Cliente frecuente | ≥ 5 compras previas | 5% adicional |
| Monto de compra | ≥ $500 | 7% adicional |
| Día de promoción | Es día especial | 15% adicional |
| **Límite máximo** | Cualquier combinación | **30% máximo** |

### Ejemplos de Cálculo

**Ejemplo 1:** Cliente nuevo, 12 productos, $450, día normal

- Descuento: 10% (solo por cantidad)

**Ejemplo 2:** Cliente frecuente, 15 productos, $600, día de promoción

- 10% (cantidad) + 5% (frecuente) + 7% (monto) + 15% (promoción) = 37%
- **Descuento aplicado: 30%** (límite máximo)

**Ejemplo 3:** Cliente frecuente, 8 productos, $300, día normal

- Descuento: 5% (solo cliente frecuente)

## 🔧 Requisitos Técnicos Cumplidos

### 1. Uso de Condicionales

- ✅ Estructuras `if` para evaluar cada criterio de descuento
- ✅ Validación de entrada de datos con manejo de excepciones

### 2. Subcondiciones

- ✅ Evaluación independiente de cada criterio de descuento
- ✅ Acumulación de descuentos según condiciones múltiples

### 3. Condiciones de Borde

- ✅ Maneja **exactamente 10 productos** (operador `>=`)
- ✅ Maneja **exactamente 5 compras previas** (operador `>=`)
- ✅ Maneja **exactamente $500** (operador `>=`)

### 4. Condiciones Anidadas

- ✅ Evaluación secuencial de múltiples condiciones verdaderas
- ✅ Límite de descuento máximo del 30%

### 5. Salida Controlada

- ✅ Si ninguna condición se cumple, descuento = 0%
- ✅ Resumen detallado de la compra

### 6. Convención de Nombres

- ✅ Todas las variables y funciones usan `snake_case`
- ✅ Código documentado con docstrings

## 🚀 Instalación y Uso

### Requisitos Previos

- Python 3.6 o superior

### Ejecución del Programa

```bash
python ae3_apb_ejercicio_individual.py
```

### Flujo de Uso

1. **Ingreso de datos iniciales:**
   - Cantidad de compras previas del cliente
   - Si es día de promoción especial (sí/no)

2. **Ingreso de productos:**
   - Ingrese el precio de cada producto
   - Ingrese `0` para finalizar la compra

3. **Visualización de resultados:**
   - Total acumulado por cada producto
   - Descuento acumulado después de cada producto
   - Resumen final con descuento total aplicado

### Ejemplo de Ejecución

```text
Ingrese la cantidad de veces que ha comprado antes: 6
¿Es un día de promoción especial? (sí/no): si
Ingrese el precio de cada producto. Para terminar, ingrese 0.
Precio del producto (o 0 para terminar): 50
Total acumulado: $50.00
Descuento acumulado: 5% ($2.50)

Precio del producto (o 0 para terminar): 50
Total acumulado: $100.00
Descuento acumulado: 5% ($5.00)

...

--- Resumen Final ---
Total de productos: 12
Monto total: $600.00
Descuento final aplicado: 30% ($180.00)
Total a pagar: $420.00
```

### Variables Principales

- `PRODUCT_QTY`: Contador de productos ingresados
- `TOTAL_SUM`: Suma acumulada del total de la compra
- `times_bought_input`: Historial de compras del cliente
- `sale_day_input`: Indicador de día promocional

## 📈 Diagrama de Flujo

El programa sigue la lógica representada en el diagrama de flujo adjunto, evaluando secuencialmente cada condición:

1. **¿Cantidad > 10?** → +10% descuento
2. **¿Compras previas > 5?** → +5% descuento
3. **¿Total > $500?** → +7% descuento
4. **¿Día de promoción?** → +15% descuento
5. **Límite a 30%** → Retornar descuento final

## 🛡️ Manejo de Errores

- Validación de entrada numérica con `try-except`
- Rechazo de precios negativos
- Mensajes informativos para el usuario

## 📚 Documentación Adicional

Para documentación detallada del código, visite:

- **Wiki del Proyecto:** [DeepWiki - M3_AE3_ABP-Ejercicio-individual](https://deepwiki.com/schiesscl/M3_AE3_ABP-Ejercicio-individual)

## 📄 Licencia

Este proyecto es de uso educativo.

---

## 🔍 Notas de Versión

### Versión 1.1 (Actual)

- ✅ Corrección de casos de borde (>=10, >=5, >=500)
- ✅ Simplificación de lógica lineal
- ✅ Documentación completa con docstrings
- ✅ Validación mejorada de entradas

### Versión 1.0

- Implementación inicial del sistema de descuentos
