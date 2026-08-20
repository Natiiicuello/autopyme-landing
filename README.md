[README.md](https://github.com/user-attachments/files/31258432/README.md)
# AutoPYME 🌶️

**Automatización con Inteligencia Artificial para PYMEs argentinas.**

AutoPYME diseña agentes de IA a medida — como **Pimienta**, nuestro propio agente — para que cada PYME tenga atención comercial 24/7, cotización automática y registro de cada consulta, sin depender de que una persona esté siempre disponible.

🔗 **Sitio en vivo:** [autopymeia.netlify.app](https://autopymeia.netlify.app/)
💬 **Probar a Pimienta (demo real):** [t.me/Autopim_bot](https://t.me/Autopim_bot)

---

## El problema

Un cliente escribe a las 22hs y no recibe respuesta a tiempo → le compra al competidor.
Cada presupuesto hecho a mano lleva 20 minutos que deberían ir a cerrar ventas.
Si la persona encargada falta un día, la consulta se frena y la venta se pierde con ella.

## La solución

No vendemos un bot genérico. **Para cada cliente construimos un agente distinto**, entrenado con su catálogo, sus reglas de negocio y su tono. Pimienta es el nuestro — lo usamos como ejemplo vivo de lo que armamos a medida para cada PYME.

Cada agente:
- Atiende consultas y cotiza en tiempo real, en **Pesos Argentinos ($ARS)**.
- Guarda automáticamente cada conversación en **Google Sheets**.
- Dispara alertas en **Slack** apenas entra una consulta nueva.
- Deriva a un humano cuando la consulta se sale de lo que puede responder con seguridad.

## Cómo se construye (metodología)

1. **Diagnóstico** — mapeamos dónde se pierden consultas y qué preguntas se repiten.
2. **Configuración del agente** — diseñamos el prompt con la metodología **OCFE** (Objetivo · Contexto · Formato · Ejemplos), definiendo reglas, tono rioplatense y límites de respuesta. Se prueba a fondo antes de salir a producción, porque un flujo automatizado no se corrige en vivo.
3. **Integración de flujo** — conectamos webhooks en **Make / n8n** con Telegram, Google Sheets y Slack.
4. **Lanzamiento en vivo** — el agente empieza a operar 24/7 en la nube.

## Stack

| Capa | Tecnología |
|---|---|
| Automatización / orquestación | Make, n8n |
| Canal de atención | Telegram |
| Persistencia de datos | Google Sheets |
| Notificaciones internas | Slack |
| Landing page | HTML / CSS / JS (vanilla) |
| Hosting | Netlify |

## Filosofía: cero humo

- **MVP ultra-estable**, simple de entender y difícil de romper.
- **Demo-First**: si algo no se puede mostrar funcionando, no se promete.
- **Regla de oro**: si no le ahorra tiempo al cliente, no sale a producción.

## Cumplimiento legal

Alineado a la **Ley 25.326 de Protección de Datos Personales** (Argentina). Se solicita únicamente la información necesaria para atender cada pedido — sin datos sensibles de más.

## Estructura del repo

```
/
├── index.html      # Landing page completa (HTML/CSS/JS en un solo archivo)
└── README.md        # Este archivo
```

## Roadmap

- [ ] Catálogo dinámico conectado por rubro (más allá de la demo con catálogo fijo)
- [ ] Panel simple para que cada cliente vea sus propias métricas de uso
- [ ] Más canales por agente: WhatsApp e Instagram además de Telegram

---

**AutoPYME** · Hecho en Argentina 🇦🇷 · Proyecto nacido dentro de CoderCup
