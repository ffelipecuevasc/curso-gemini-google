# AGENTS.md

Instrucciones obligatorias para cualquier agente de IA que trabaje en este repositorio.

## 1. Lectura obligatoria antes de actuar

Antes de analizar, proponer o modificar cualquier cosa, **debes leer completos**:

1. `README.md`: qué es el proyecto, su estructura y sus tecnologías.
2. `DESIGN.md`: sistema de diseño visual que todo cambio debe respetar.

No escribas código ni propongas cambios sin haber leído ambos archivos.

## 2. Restricción de Git

- **PROHIBIDO** ejecutar `git commit`.
- **PROHIBIDO** ejecutar `git push`.

El desarrollador es el único que realiza commits y pushes.

## 3. Mensaje de commit obligatorio

Cada vez que realices **cualquier cambio de código**, termina tu respuesta con un mensaje de commit para que el desarrollador lo use:

- Máximo **100 caracteres**.
- Sencillo, claro y en modo imperativo.
- En un bloque de código al final de la respuesta.

Ejemplo:

```
Agrega sección de preguntas frecuentes con acordeón
```

Si no hubo cambios de código, no incluyas mensaje de commit.

## 4. Convenciones del proyecto

- Respeta el diseño descrito en `DESIGN.md` (minimalismo, tipografía, paleta, modo claro y oscuro).
- Mantén la estructura de archivo único `index.html`, salvo que se indique lo contrario.
- Si un cambio afecta la estructura o las funciones del proyecto, indícalo para actualizar `README.md`.