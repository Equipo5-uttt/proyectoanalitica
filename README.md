## Proyecto Sistema de Autorización - Validación en 5 Pasos

## Descripción

Este proyecto implementa un sistema para validar la autorización de servicios de salud (consultas, procedimientos, medicamentos, insumos) consultando información en hojas de cálculo públicas de Google Sheets. Simula un proceso de autorización en 5 pasos, 
determinando si un servicio está cubierto directamente o si requiere autorización manual.

## ¿Por qué este proyecto?

Este proyecto fue creado como una práctica para demostrar los conocimientos de phyton aplicados en escenarios reales y cómo estructurar proyectos simples

## Uso

1. El sistema carga datos de diversas hojas de cálculo públicas de Google Sheets, que contienen información sobre servicios capitados y exclusiones.
2. Permite al usuario ingresar la ciudad de residencia, la IPS primaria y el código o nombre del servicio. Luego, busca la información del servicio en las hojas de cálculo relevantes.
3. Si el servicio es encontrado en las tablas de prestación directa, el sistema muestra los detalles correspondientes. Si no es encontrado, solicita información adicional (IPS que remite y diagnóstico) e indica que se requiere una autorización manual.

4. La implementación incluye lógica para:
- Cargar múltiples hojas de cálculo desde URLs públicas.
- Leer todas las hojas dentro de cada archivo de Excel.
- Intentar identificar columnas relevantes (como "CODIGO CUPS", "DESCRIPCION SERVICIO", "MEDICAMENTOS", etc.) incluso si los nombres varían ligeramente.
- Filtrar datos para la búsqueda.
- Guiar al usuario a través de un proceso interactivo de 5 pasos.

## Requisitos

1. Python 3.6 o superior
2. Las librerías `pandas` y `requests`.
