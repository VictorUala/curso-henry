# 📂 HANDOVER: Puente de Memoria (Antigravity <-> Claude)

## 🕒 Última Actualización: 2026-04-05
**Agente Responsable:** Claude Code (CLI)
**Estado del Proyecto:** Entorno completamente verificado. Todo operativo. Listo para comenzar ejercicios del curso.

---

## 🎯 Contexto para el Siguiente Agente (Claude/Gemini)
¡Hola! Estás entrando en el curso de **Soy Henry** de Víctor. El entorno ya está configurado y verificado.

**REGLA DE ORO:** Antes de hacer nada, **lee este archivo**, `CLAUDE.md` y `CONTEXTO.md`. No dupliques tareas que ya figuren como "Completadas" aquí.

**IMPORTANTE:** Víctor acaba de migrar del chat visual (extensión VS Code) al **CLI de Claude Code**. Es su primera sesión en el CLI. Está adaptándose a la interfaz pero decidió quedarse con el CLI por estabilidad y acceso a más herramientas.

---

## 🛠️ Estado de la Infraestructura

### Verificado y Operativo (2026-04-05)
- **n8n:** Instancia activa en **Railway** → `https://primary-production-3de5.up.railway.app`
  - API Key configurada en `settings.json`
  - Workflow existente: `kiW1qzYP1C1Y8N6B | "Sarasa" | activo: true`
- **GitHub:** Conectado a `git@github.com:VictorUala/curso-henry.git`
  - Último commit: `6c42cec — Setup inicial del workspace`
  - Rama: `master`. Repo limpio, sin pendientes.
- **MCP n8n:** Instalado en `C:\Users\Victor\AppData\Roaming\npm\node_modules\n8n-mcp\`
  - Configurado en `C:\Users\Victor\.claude\settings.json`
  - Nota: los tools MCP se cargan al iniciar la sesión. Si no aparecen, reiniciar el CLI.
- **Excalidraw / Mermaid:** Configurado en sesión anterior de AntiGravity (Gemini).
  - Víctor tiene extensión de Excalidraw en VS Code para visualizar los archivos.
  - **PENDIENTE:** Víctor va a traer los detalles de configuración de esa sesión de AntiGravity para documentarlo aquí. Es una prioridad al inicio de la próxima sesión.
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

---

## ⏳ Próximos Pasos (en orden de prioridad)

1. **[ ] Documentar configuración de Excalidraw/Mermaid** — Víctor trae los datos de la sesión AntiGravity
2. **[ ] Comenzar ejercicios del curso Soy Henry** — Víctor indica en qué lección está
3. **[ ] Definir arquitectura del Proyecto Integrador** — cuando corresponda en el curso

---

## 📝 Notas Pedagógicas
- El enfoque debe ser **Pedagógico y Senior**. No buscamos solo "hacer", sino "enseñar a defender" el proyecto ante un Tech Lead de Mercado Libre.
- Priorizar **solidez conceptual** en flujos agénticos y Prompt Engineering.
- Víctor tiene background en electrónica y BASIC desde los 80s. Puede recibir analogías técnicas.
