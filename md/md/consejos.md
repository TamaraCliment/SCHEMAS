# Cosas a tener en cuenta:

!!! warning "¡Atención!"
    Asegúrate de validar tu XML antes de enviarlo.

!!! warning "¡Atención!"
    Se validan los xml no los xsd.


!!! tip "Consejo útil"
    Utiliza las tabulaciones y los comentarios, te seran de gran ayuda. 

# Proceso de validación de XML contra XSD

A continuación se muestra el diagrama de flujo que representa el proceso de validación de un archivo XML utilizando un archivo XSD:

``` mermaid
  graph TD
    A[Inicio] --> B[Leer archivo XML]
    B --> C[Leer archivo XSD]
    C --> D[Validar XML contra XSD]
    D -->|Validación exitosa| E[Generar reporte de éxito]
    D -->|Error de validación| F[Generar reporte de error]
    E --> G[Finalizar]
    F --> G[Finalizar]

```

