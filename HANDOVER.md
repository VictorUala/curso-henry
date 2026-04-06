# 📂 HANDOVER: Puente de Memoria (Antigravity <-> Claude)

## 🕒 Última Actualización: 2026-04-06 (sesión mañana)
**Agente Responsable:** Claude Code (CLI) — Opus 4.6
**Estado del Proyecto:** MCPs operativos (Excalidraw + n8n). Diagrama de flujo pendiente de regenerar con MCP. Próximo paso inmediato: generar diagrama completo BrightHome con `create_flowchart` del MCP Excalidraw.

---

## 🎯 Contexto para el Siguiente Agente (Claude/Gemini)
¡Hola! Estás entrando en el curso de **Soy Henry** de Víctor. El entorno ya está configurado y verificado.

**REGLA DE ORO:** Antes de hacer nada, **lee este archivo**, `CLAUDE.md` y `CONTEXTO.md`. No dupliques tareas que ya figuren como "Completadas" aquí.

**IMPORTANTE:** Víctor migró del chat visual (extensión VS Code) al **CLI de Claude Code**. Ya lleva varias sesiones en el CLI y está cómodo con él. Eligió el CLI por estabilidad y acceso a más herramientas.

---

## 🛠️ Estado de la Infraestructura

### Verificado y Operativo (2026-04-06)
- **n8n:** Instancia activa en **Railway** → `https://primary-production-3de5.up.railway.app`
  - API Key configurada en `settings.json`
  - Workflow existente: `kiW1qzYP1C1Y8N6B | "Sarasa" | activo: true`
- **GitHub:** Conectado a `git@github.com:VictorUala/curso-henry.git`
  - Último commit: `6c42cec — Setup inicial del workspace`
  - Rama: `master`. Repo limpio, sin pendientes.
- **MCP n8n:** Instalado y operativo (verificado 2026-04-06).
  - Configurado en `C:\Users\Victor\.claude\settings.json` bajo `mcpServers.n8n`
- **MCP Excalidraw:** Instalado y operativo (verificado 2026-04-06).
  - Configurado en `C:\Users\Victor\.claude\settings.json` bajo `mcpServers.excalidraw`
  - Comando: `C:\Program Files\Python311\Scripts\excalidraw-mcp.exe`
  - Test "Hola Mundo" exitoso: generó `test-mcp.excalidraw` con elipse azul.
  - Víctor tiene extensión de Excalidraw en VS Code para visualizar los archivos.
  - **IMPORTANTE:** Si los MCPs no cargan al iniciar el CLI, cerrar Antigravity completo y reabrir (no basta con `/exit` del CLI). Los MCPs se configuran en `settings.json`, NO en `.claude.json` (ese es archivo interno de estado del CLI, no tocarlo).
- **Permisos CLI:** `bypassPermissions` activo — Claude ejecuta sin pedir confirmación.
- **Entorno Local:** VS Code + Antigravity (Gemini) + Claude Code CLI en `z:\curso_henry`
- **Git config global:** user.name = Victor / user.email = victorhugouala@gmail.com

---

## 🏛️ Decisiones de Arquitectura

### Repositorio Git
- **Decisión:** Repo en el **root** (`z:/curso_henry/`), backup completo de todo el workspace.
- **Incluye:** proyecto integrador, ejercicios de clase, CLAUDE.md, CONTEXTO.md, HANDOVER.md.
- **Por qué:** Seguridad ante falla de PC. Backup completo > simplicidad.

### Dinámica de Trabajo entre Modelos
- **Principal:** Claude Code CLI (cuota de contexto alta, más preciso, acceso a herramientas avanzadas)
- **Auxiliar:** AntiGravity / Gemini (segunda opinión, destrabar bloqueos, soporte visual)
- **Filosofía:** Un solo chat principal por sesión. Este HANDOVER es el puente entre modelos.
- **Sobre el CLI:** Víctor eligió el CLI sobre la extensión visual por estabilidad y más herramientas. La interfaz es más "áspera" visualmente pero funciona mejor.

---

## ✅ Tareas Completadas

1. Alineación de rol "Senior AI Automation Mentor & Architect"
2. Estructura del workspace verificada (`/ejercicios-clase`, `/proyecto-integrador`)
3. Git inicializado en root, GitHub conectado y verificado
4. n8n MCP instalado y configurado
5. Conexión n8n Railway verificada (workflow "Sarasa" activo)
6. Permisos CLI configurados (`bypassPermissions`)
7. Primera sesión de Víctor en Claude Code CLI completada
8. Sistema de memoria y contexto investigado y configurado:
   - Ventana de contexto CLI: **200k tokens** (no 1M — eso es Gemini)
   - `/extra-usage` ejecutado (respondió "Login successful", no cambió el límite de contexto)
   - `/context` muestra uso actual: ~30k/200k tokens
   - Memoria nativa de Claude activada en cuenta: "Buscar conversaciones" + "Generar memoria del historial" (aplica a claude.ai web/desktop/mobile, NO al CLI)
   - Para el CLI: sistema HANDOVER + archivos `memory/` sigue siendo el puente
9. Carpeta `img/` creada en root para compartir capturas de pantalla con Claude (Claude puede leer imágenes desde ahí)

---

## ⏳ Próximos Pasos (en orden de prioridad)

1. **[x] Documentar configuración de Excalidraw/Mermaid** — Completado. Config en settings.json verificada.
2. **[x] Leer y analizar documento Proyecto Integrador** — Completado. 21 páginas, entendido completo.
3. **[x] Diagrama de flujo en Excalidraw (JSON manual)** — `diagrama-flujo-brighthome.excalidraw` (generado a mano, sin MCP). NO es compatible con el MCP — el MCP no puede leerlo/modificarlo.
4. **[x] Diagrama de flujo corregido y finalizado** — `diagrama-flujo-brighthome-v2.excalidraw` con flechas perfectas, tipografía Helvetica, colores por categoría. Generado por Claude (JSON directo) + correcciones iterativas con feedback visual de Víctor.
5. **[ ] Comenzar implementación en n8n** — Paso 1: Airtable Form + Supabase
6. **[ ] Preparar defensa en vivo** — 3 casos de prueba (positivo, negativo, sugerencia)

### Log sesión 2026-04-05 (tarde-noche)
- Víctor instaló extensión claudeboard para pegar imagenes en CLI (dkodr/claudeboard)
- Se leyó completo el PDF del Proyecto Integrador (BrightHome NPS, 21 páginas)
- Se generó diagrama de flujo en formato .excalidraw (JSON manual) con los 4 pasos y 6 caminos
- MCP de Excalidraw y n8n NO cargaron en esa sesión
- Se intentó usar `import_mermaid_flowchart` del MCP pero tardó +7 horas sin resultado — Víctor abortó
- Se cambió a modelo Opus para esta tarea (consume 2x cuota vs Sonnet)

### Log sesión 2026-04-06 (mañana)
- MCPs no cargaban al reiniciar solo el CLI. Solución: cerrar Antigravity completo y reabrir.
- Antigravity (Gemini) dijo que el archivo correcto era `.claude.json` — INCORRECTO. El archivo de config de MCPs es `settings.json`. `.claude.json` es estado interno del CLI, no tocar.
- Ambos MCPs (Excalidraw + n8n) ahora operativos y verificados.
- Test "Hola Mundo" con `create_flowchart`: exitoso, generó elipse azul correctamente.
- `read_diagram` del MCP NO puede leer el JSON manual — formato incompatible.
- Se probó MCP `create_flowchart` e `import_mermaid_flowchart` para diagrama complejo: ambos fallan o cuelgan. Mermaid importado a Excalidraw sale en B/N con tags `<br>` visibles. **El MCP de Excalidraw NO sirve para diagramas complejos.**
- **DESCUBRIMIENTO CLAVE: Claude genera excelentes diagramas escribiendo JSON de Excalidraw directo** (sin MCP, sin Mermaid). Controla coordenadas, colores, layout, tipografía. Si hay flechas desalineadas, Víctor manda captura de pantalla y Claude corrige calculando las coordenadas exactas. **Este es el Plan A para diagramas futuros.**
- **Tips técnicos aprendidos para JSON de Excalidraw:**
  - Las flechas deben tener `startBinding` y `endBinding` con el `elementId` del nodo para anclarse al borde
  - **El binding es BIDIRECCIONAL:** la flecha necesita `startBinding` → elementId, Y el nodo necesita la flecha en su `boundElements[]`. Si falta uno de los dos, la flecha no sigue al nodo al moverlo.
  - En un diamante, el vértice inferior es (x + width/2, y + height) — TODAS las flechas que salen abajo deben arrancar de ese punto exacto
  - `fontFamily: 1` = hand-drawn (Virgil), `2` = Helvetica (técnica), `3` = Cascadia (monospace)
  - `roughness: 0` da líneas limpias, sin efecto dibujado a mano
  - Extensión Excalidraw en VS Code permite editar diagramas inline — excelente integración con el workflow
- Archivos `.excalidraw` existentes en `proyecto-integrador/`:
  - `diagrama-flujo-brighthome - Original Claude.excalidraw` — backup del original manual
  - `diagrama-flujo-brighthome-v2.excalidraw` — **VERSIÓN FINAL**: corregida con flechas perfectas + tipografía Helvetica
  - `diagrama-flujo-brighthome.excalidraw` — sobreescrito por Antigravity (no usar)
  - `diagrama-flujo-brighthome-GEMINI.excalidraw` — generado por Antigravity (inferior)
  - `diagrama-flujo-brighthome.mmd` — código Mermaid (para documentación)
  - `test-mcp.excalidraw` — test "Hola Mundo" (descartable)
- **PRÓXIMO PASO:** Comenzar implementación en n8n. El flujo tiene 4 pasos y 5 caminos + error:
  - PASO 1: Entrada (Airtable Form trigger NPS 1-10) + Enriquecimiento (Supabase) + Merge payload
  - PASO 2: Análisis IA (OpenAI: sentimiento, categoría, resumen, acción)
  - PASO 3: Agente Router por categoría + Log en Google Sheets (todos los casos)
  - PASO 4: 5 caminos de acción + revisión manual
    - Camino 1: satisfaccion (NPS 9-10) → Airtable "Clientes felices" + email agradecimiento
    - Camino 2: sugerencia (NPS 7-8) → IA etiqueta temática + Airtable "Sugerencias"
    - Camino 3: observacion (NPS 7-8) → Airtable "Observaciones"
    - Camino 4: falla_tecnica (NPS 0-6) → Airtable "Soporte" + email interno + ticket abierto
    - Camino 5: reclamo (NPS 0-6) → Airtable "Reclamos" + email alerta + disculpa + prioridad alta
    - Revisión manual: error/JSON inválido → Google Sheets pendiente + Slack + email alerta
  - SEGUIMIENTO: Schedule trigger cada X horas, si detractor no contactado en 48hs → alerta Slack

---

## 📝 Notas Pedagógicas
- El enfoque debe ser **Pedagógico y Senior**. No buscamos solo "hacer", sino "enseñar a defender" el proyecto ante un Tech Lead de Mercado Libre.
- Priorizar **solidez conceptual** en flujos agénticos y Prompt Engineering.
- Víctor tiene background en electrónica y BASIC desde los 80s. Puede recibir analogías técnicas.
