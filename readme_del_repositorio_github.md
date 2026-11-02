# Digital Health - Sistema de Automatización de Facturación en Excel VBA

Proyecto académico correspondiente al curso **Introduction to Computer Literacy** (USIL), orientado a la automatización del proceso de captura de datos, validación y emisión de comprobantes de pago para la clínica virtual *Digital Health*.

## 📌 Descripción del Proyecto

El sistema reemplaza el registro administrativo manual mediante una solución ofimática en **Microsoft Excel (.xlsm)** programada en **Visual Basic for Applications (VBA)**. Permite ingresar información de pacientes, validar en tiempo real formatos de identificación tributaria (DNI / RUC), clasificar el tipo de comprobante (Boleta o Factura) y registrar las operaciones en una base de datos tabular local.

## 📁 Contenido del Repositorio

* **`Digital_Health_Facturacion.xlsm`** *(nombre del libro subido)*: Libro de Excel habilitado para macros que contiene:
  * Hoja de cálculo configurada como repositorio tabular para el almacenamiento de registros.
  * Formulario principal de captura y validaciones (`UserForm1`).
  * Módulo visual de generación/vista de comprobante (`UserForm_Boleta`).

## ⚙️ Funcionalidades Implementadas en el Código Actual

El código fuente compilado dentro del libro incluye la lógica de los siguientes módulos:

1. **`UserForm1` (Módulo de Facturación y Registro):**
   * **Carga automatizada de catálogos:** Inicialización de combos (`cboAtencion`, `cboMetodo`, `cboComprobante`).
   * **Validación de identidad:** Control de longitud exacta para el DNI (8 dígitos numéricos) y teléfono móvil (9 dígitos).
   * **Lógica condicional tributaria:** 
     * Si se selecciona **Boleta**, los campos de RUC y Razón Social quedan bloqueados y limpios.
     * Si se selecciona **Factura**, se desbloquean y se valida que el RUC contenga 11 dígitos numéricos obligatorios.
   * **Persistencia de datos:** Búsqueda dinámica de la última fila libre e inserción consecutiva de registros en la hoja de Excel.
   * **Limpieza de formulario:** Procedimiento `btnLimpiar_Click` para restablecer los controles a su estado inicial.

2. **`UserForm_Boleta` (Vista de Comprobante):**
   * Visualización estructurada de los datos capturados y botón de cierre (`btnCerrarBoleta`).

> **Nota de alcance:** Los módulos adicionales de Gestión de Capital (`UserForm_Validacion`, `UserForm_Movimientos`, `UserForm_Resumen`) forman parte de la arquitectura y diseño de prototipos del proyecto general, encontrándose actualmente en fase de especificación para las siguientes entregas.

## 🚀 Requisitos de Ejecución

* **Sistema Operativo:** Windows 10 u 11 (64 bits).
* **Aplicación:** Microsoft Excel (Microsoft 365, Office 2019 / 2021).
* **Seguridad:** Habilitar macros al abrir el archivo (`.xlsm`).

## 🛠️ Instrucciones de Uso

1. Descarga o clona el repositorio en tu equipo.
2. Abre el archivo `.xlsm` en Microsoft Excel.
3. En la barra de advertencia de seguridad superior, haz clic en **"Habilitar contenido"** para permitir la ejecución del código VBA.
4. Presiona `ALT + F11` para abrir el entorno de Visual Basic for Applications y explorar el código o ejecuta el formulario `UserForm1`.

## 👥 Integrantes del Equipo

* **Diaz Seki, Bruno Seiya**
* **Espiritu Curo, Jeff Smith**
* **Luyo Soto, José Francesco Felix**
* **Tejada Rivera, Erick Henry**
* **Vasquez Cuya, Johan Estefano**

*Universidad San Ignacio de Loyola (USIL) — 2026-II*