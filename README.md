# 🤖 Sistema expertoq de Inventario

Sistema experto basado en reglas de inferencia para la gestión automatizada, análisis y toma de decisiones sobre inventarios de retail a gran escala. Diseñado para simular el entorno de un supermercado, evaluando más de 130 productos bajo 25 reglas de negocio distintas.

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![GUI](https://img.shields.io/badge/GUI-CustomTkinter-orange.svg)

---

## ✨ Características Principales

- 🔍 **Búsqueda Inteligente (Fuzzy Search)**: Encuentra productos escribiendo palabras clave parciales (ej: escribir "leche" muestra Leche Entera, Deslactosada y de Almendra).
- ⚙️ **Motor de Inferencia Robusto**: Evalúa 25 reglas de negocio que consideran: nivel de stock, demanda, tiempo de entrega, caducidad, tipo de producto, margen de ganancia y dependencia de proveedor.
- 🖥️ **Interfaz Gráfica Moderna (GUI)**: Desarrollada con `CustomTkinter` en modo oscuro, intuitiva y responsiva.
- 📊 **Reportes Automatizados**: Escanea todo el inventario y genera alertas clasificadas por prioridad (Urgente, Alta, Media, Baja).
- 📋 **Historial de Evaluaciones**: Guarda un registro de todas las evaluaciones manuales realizadas durante la sesión para auditoría o revisión.
- 📦 **Base de Conocimiento Escalable**: Estructura en JSON fácil de ampliar con nuevos productos o reglas sin modificar el código fuente.

---

## 🛠️ Tecnologías Utilizadas

- **Lenguaje**: Python 3.11+
- **Interfaz Gráfica**: `customtkinter` (Tkinter modernizado)
- **Manejo de Datos**: `json`, `unicodedata` (para normalización de texto)
- **Control de Versiones**: Git & GitHub

---

## 🚀 Instalación y Uso

Sigue estos pasos para ejecutar el proyecto en tu máquina local:

1. **Clona el repositorio**:
   ```bash
   git clone https://github.com/Leandro7856/SistemaExperto-inventario.git

---

## Instalacion de dependencias
 pip install customtkinter

---

## Ejecutar la aplicacion de forma correcta
python main.py

---

## Ejemplo de uso del sistema
Consulta Rápida: Ve a "Consultar Producto" y escribe "yogurt". El sistema mostrará los productos coincidentes y las alertas aplicables (ej: liquidación por caducidad).

---

## 🛠️ Estructura del sistema

<img width="762" height="277" alt="image" src="https://github.com/user-attachments/assets/b69cc613-2bcb-421d-9a1d-83fe6112cdf2" />

---

## 📝 Reglas agregadas en el Parcial 2

Se agregaron dos nuevas reglas al sistema experto para cubrir escenarios adicionales del dominio de inventario Walmart:
Regla 26 (2 condiciones unidas por Y)
SI el tipo de producto es perecedero Y el nivel de stock es critico
ENTONCES retirar producto de venta inmediatamente y donar
Explicación: Un producto perecedero con stock crítico está a punto de agotarse y vencerse. Es mejor retirarlo y donarlo para beneficio fiscal que arriesgar una venta fallida.
Prioridad: Urgente
Regla 27 (3 condiciones unidas por Y)
SI el margen de ganancia es alto Y la demanda es estacional_alta Y el nivel de stock es medio
ENTONCES aumentar stock de seguridad un 50% y asegurar proveedor alternativo
Explicación: Producto muy rentable en temporada alta con stock moderado. Cada unidad no vendida es ganancia perdida, se debe maximizar disponibilidad.
Prioridad: Alta

---

## Captura de ejecución del sistema

<img width="921" height="565" alt="image" src="https://github.com/user-attachments/assets/19615b33-7f01-4123-ba4b-25b2b8663453" />

---


