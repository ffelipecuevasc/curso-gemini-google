<div align="center">

# Gemini y Google en el entorno laboral

Portal educativo de apoyo para el curso sobre el ecosistema de IA de Google.

</div>

---

## Acerca del proyecto

Sitio web de una sola página que reúne los recursos del curso: una introducción a Gemini y Google Workspace, la familia de modelos, NotebookLM, guías descargables y videos de apoyo.

Su diseño se inspira en la interfaz de Google Gemini: minimalista, con mucho espacio en blanco, geometría redondeada y una iluminación azul tenue de fondo.

## Contenido

- **Inicio:** presentación y cápsula de prompt interactiva con respuestas simuladas.
- **Ecosistema:** cómo Gemini se integra en Gmail, Docs, Sheets, Drive y Meet.
- **Modelos:** comparativa de Gemini Flash, Pro y Ultra.
- **NotebookLM:** investigación y productividad con fuentes ancladas.
- **Recursos:** guías en PDF y videos de apoyo.
- **Instructor:** información de Felipe Cuevas.

## Características

- Modo claro y oscuro, con persistencia de la preferencia del usuario
- Diseño responsivo con menú móvil
- Selector de modelo y sugerencias rápidas en el prompt
- Modal de video y avisos de descarga
- Sin dependencias de compilación: abre `index.html` y listo

## Tecnologías

| Herramienta | Uso |
|---|---|
| HTML5 | Estructura semántica |
| Tailwind CSS (CDN) | Estilos |
| JavaScript (ES6+) | Interactividad |
| Google Fonts | Tipografía (Outfit e Inter como alternativa a Google Sans) |

## Uso local

```bash
git clone <URL-DEL-REPOSITORIO>
cd <NOMBRE-DEL-REPOSITORIO>
```

Abre `index.html` en tu navegador. Si prefieres un servidor local:

```bash
python3 -m http.server 8000
```

Luego visita `http://localhost:8000`.

## Estructura

```
.
├── index.html    # Sitio completo (HTML, estilos y scripts)
├── DESIGN.md     # Guía de diseño visual
├── AGENTS.md     # Reglas para agentes de IA
└── README.md
```

## Diseño

Los principios visuales (colores, tipografía, espaciado, sombras y luz ambiental) están documentados en [`DESIGN.md`](DESIGN.md).

## Autor

**Felipe Cuevas**: Consultor y facilitador de IA en entornos profesionales.

---

<div align="center">
<sub>Proyecto con fines educativos. Gemini, Google y NotebookLM son marcas de Google LLC.</sub>
</div>