---
name: lex-juris-search
description: Conssolidated Motor de Búsqueda Soberana (Infoleg, SAIJ, HuggingFace).
---

# Skill: Lex Juris Search (GOLD Edition)

Este motor de búsqueda orquestado garantiza que las consultas legales se expandan de forma semántica y se clasifiquen por jerarquía normativa en la República Argentina.

## Flujo de Inteligencia Semántica
1.  **Expansión por Tesauro**: Antes de consultar el dataset, la query se cruza con el Tesauro SAIJ Soberano (`fjzubq-glitch/Tesauro-Saij-PRO.`).
    -   *Ejemplo*: "Amparo" -> "Garantías Constitucionales", "Acción de Clase".
2.  **Mapeo de Fuentes**:
    -   **Leyes**: Se utiliza Infoleg (URL oficial) y se ofrece versión limpia vía espejo `fjzubq-glitch/Normas-Ar-Master`.
    -   **Jurisprudencia**: Se vincula al repositorio espejo `fjzubq-glitch/Lex-Sovereign-Data.`.
    -   **Conceptos**: Se utiliza el "Resumen Inteligente" estilo Hernán CC para definiciones técnicas.

## Jerarquía de Resultados
1.  **Fundamentos (Constitución/Tratados)**.
2.  **Leyes Nacionales (Infoleg/Normas-Ar-Master)**.
3.  **Jurisprudencia (Lex-Sovereign-Data.)**.
4.  **Doctrina/Resúmenes (Hernán CC Style)**.

## Reglas de Implementación
-   Uso de tipografía **Mono-espaciada** para metadatos técnicos (rutas de archivo, comandos).
-   Uso de **Inter/Sans-serif** para el cuerpo de la ley.
-   El sistema siempre debe devolver al menos una ley, un fallo y una definición técnica si el término existe en el Tesauro.
