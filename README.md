# Supermercados Diguillín · datos crudos

Datos del caso de estudio de la asignatura **Minería de Datos (IEI-097)**, Ingeniería en
Informática, IP Santo Tomás Chillán. Supermercados Diguillín es una empresa **ficticia**; todos
los datos son **sintéticos**, generados por código con semilla fija. No corresponden a personas
ni transacciones reales.

## Archivos (`crudo/`)

| Archivo | Filas | Qué es |
|---|---|---|
| `clientes.csv` | 1.245 | Socios de la Tarjeta Vecino, tal como salieron del sistema |
| `boletas.csv` | 57.527 | Boletas de doce meses |
| `detalle_boletas.csv` | — | Líneas de cada boleta (producto, cantidad, precio) |
| `productos.csv` | — | Catálogo de productos |
| `locales.csv` | — | Los locales de la cadena |

Los archivos **crudos traen errores a propósito** (texto inconsistente, faltantes, duplicados,
claves foráneas huérfanas, fechas imposibles, totales negativos): limpiarlos es parte del curso.

## Uso desde Google Colab

```python
import pandas as pd
RUTA_DATOS = "https://raw.githubusercontent.com/de-mag-ia/diguillin-datos/main/crudo/"
clientes = pd.read_csv(RUTA_DATOS + "clientes.csv")
boletas  = pd.read_csv(RUTA_DATOS + "boletas.csv")
```

**Regla del curso:** el CSV crudo no se toca. Todo lo que se limpia se guarda con otro nombre.

Material docente de uso educativo. Docente: Waldo Ledesma.
