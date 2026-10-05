# 📧 n8n Email AI Autoresponder (PostgreSQL + Local LLM / OpenAI API)

Sistema empresarial de respuesta e interacción automática por correo electrónico mediante **n8n**, impulsado por un **Agente de IA** con conexión en tiempo real a bases de datos **PostgreSQL**.

Permite automatizar la atención de soporte, logística o atención al cliente por email de forma 100% autónoma, verídica y sin alucinaciones.

---

## ✨ Características Principales

- 📩 **Monitoreo Automático de Inbox (IMAP):** Escucha y procesa correos entrantes en tiempo real.
- 🧠 **Agente de IA Contextual (LangChain / n8n Agent):** Comprende la intención del remitente y decide de forma autónoma cuándo consultar la base de datos empresarial.
- 🗄️ **Consultas a BBDD en Tiempo Real (PostgreSQL Tool):** El agente extrae automáticamente el estado de pedidos, inventario o datos de clientes para responder con información 100% verídica.
- ✉️ **Respuesta Formal Automática (SMTP):** Genera y envía respuestas de correo con formato profesional, firma corporativa y extracción automática del remitente vía Expresiones Regulares.
- 🔒 **Privacidad Total (On-Premise):** Integrable con servidores de inferencia locales (LM Studio / vLLM / Ollama) o APIs compatibles.

---

## 🛠️ Stack Tecnológico

| Componente | Tecnología |
|---|---|
| Orquestador de Automatizaciones | n8n |
| Lectura / Entrada de Email | IMAP Trigger |
| Envío / Salida de Email | SMTP Send Node |
| Base de Datos | PostgreSQL (`postgresTool`) |
| Motor de IA | LM Studio / Ollama / OpenAI API Compatible |

---

## 🏗️ Arquitectura del Sistema

```text
📩 Correo Entrante (Cliente / Proveedor)
       │
       ▼
📫 Email Trigger (n8n IMAP)
       │
       ▼
🤖 AI Agent (Orquestador Principal)
       ├── 🧠 Motor LLM (LM Studio / vLLM local)
       └── 🗄️ Postgres SQL Tool (Consultas de pedidos y stock)
       │
       ▼
✉️ Send Email Node (n8n SMTP)
       │
       ▼
📤 Respuesta Formal Enviada al Remitente
```

---

## 📁 Estructura del Repositorio

- `workflows/`: Archivo `.json` exportado listo para importar directamente en n8n (`email_ai_autoresponder.json`).
- `docs/`: Diagramas de flujo y guías de despliegue.

---

## 👤 Autor

**Ignacio** — [GitHub Profile](https://github.com/nachovillatech)
