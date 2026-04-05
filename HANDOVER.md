# 📂 HANDOVER: Puente de Memoria (Antigravity <-> Claude)

## 🕒 Última Actualización: 2026-04-04
**Agente Responsable:** Claude Code
**Estado del Proyecto:** Setup de entorno completado. Git inicializado. Pendiente conexión con GitHub.

---

## 🎯 Contexto para el Siguiente Agente (Claude/Gemini)
¡Hola! Estás entrando en el curso de **Soy Henry** de Víctor. Acabamos de configurar la dinámica de trabajo. 

**REGLA DE ORO:** Víctor está alternando entre modelos. Antes de hacer nada, **lee este archivo**, `.clinerules` y `CONTEXTO.md`. No dupliques tareas que ya figuren como "Completadas" aquí.

---

## 🛠️ Estado de la Infraestructura
- **n8n:** Instancia activa en **Railway** (proporcionada por Víctor).
- **Entorno Local:** VS Code configurado con Antigravity y Claude Code en `z:\curso_henry`.
- **Git:** Inicializado en el **root** `z:/curso_henry/` (decisión tomada con Claude — ver sección de decisiones abajo).
- **Git config global:** user.name = Victor / user.email = victorhugouala@gmail.com
- **GitHub:** Pendiente de conexión. Hay que crear repo en GitHub y hacer `git remote add origin <url>`.

---

## 🏛️ Decisiones de Arquitectura

### Repositorio Git — ¿Root o /proyecto-integrador?
- **Decisión:** Repo en el **root** (`z:/curso_henry/`), sin `.gitignore` para excluir ejercicios.
- **Por qué:** Se quiere backup completo en GitHub de todo el workspace: proyecto integrador, ejercicios de clase, CLAUDE.md, CONTEXTO.md y HANDOVER.md. Si el repo estuviera en `/proyecto-integrador`, todos los ejercicios y archivos de configuración quedarían fuera y se perderían ante un problema con la PC.
- **Alternativa descartada:** AntiGravity había sugerido repo dentro de `/proyecto-integrador` para simplificar (sin necesidad de `.gitignore`). Se descartó porque no cubre el backup completo.

### Dinámica de Trabajo entre Modelos
- **Principal:** Claude Code (cuota de contexto alta, más preciso en programación)
- **Auxiliar:** AntiGravity / Gemini (nativo del entorno, segunda opinión, destrabar bloqueos)
- **Filosofía:** Un solo chat principal por sesión. No saltar constantemente entre modelos.

---

## ✅ Tareas Completadas (Sesión Actual)
1. **Alineación de Rol:** Se confirmó el perfil de **"Senior AI Automation Mentor & Architect"**.
2. **Sincronización de Reglas:** Lectura y adopción de `.clinerules` y `CONTEXTO.md`.
3. **Creación del Handover:** (Este archivo) Inicializado para permitir la alternancia fluida entre Antigravity y Claude.
4. **Verificación de Estructura:** Se detectaron las carpetas `/ejercicios-clase` y `/proyecto-integrador`.

---

## ⏳ Tareas Pendientes / Próximos Pasos
- [ ] Crear repo en GitHub y conectar: `git remote add origin <url>` + primer `git push`
- [ ] Comenzar con los ejercicios de clase del curso Soy Henry
- [ ] Definir arquitectura del Proyecto Integrador cuando corresponda

---

## 📝 Notas de Arquitectura
- El enfoque debe ser **Pedagógico y Senior**. No buscamos solo "hacer", sino "enseñar a defender" el proyecto ante un Tech Lead de Mercado Libre.
- Se debe priorizar la **solidez conceptual** en flujos agenticos y Prompt Engineering.
