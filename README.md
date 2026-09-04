# Help Desk Simulation

Simulación de un IT Help Desk / Service Desk para portfolio de transición a IT Support.

## Cómo funciona

- Una VM Windows 11 (**WIN11-USER01**) hace de puesto de trabajo de una usuaria ficticia, **Maria Garcia** (departamento Finance, empresa ficticia Fabrikam Inc).
- Los tickets **reales** viven en Jira Service Management (proyecto **HD**, tipo *IT Service Management*), no en este repositorio. Este repo es la documentación y el escaparate del portfolio: capturas, vídeos de troubleshooting y el contenido de cada ticket en formato legible.
- Cada incidente se inyecta de forma controlada en la VM, se aborda como lo haría un técnico real (descartando hipótesis paso a paso) y se documenta en Jira con las secciones Investigation → Root Cause → Resolution → Verification antes de cerrarlo.

## Estructura

```
help-desk-simulation/
├── tickets/           # Espejo en Markdown de cada ticket de Jira (HD-1, HD-2, ...)
├── evidence/
│   ├── screenshots/   # Capturas del troubleshooting
│   └── videos/        # Grabaciones de pantalla (o enlaces si son pesadas)
├── knowledge-base/     # Artículos reutilizables (ej. "cómo diagnosticar fallos DNS")
└── documentation/      # Configuración de la VM, scripts PowerShell, notas técnicas
```

## Tickets del portfolio

| ID | Resumen | Tipo | Estado |
|---|---|---|---|
| HD-1 | Unable to access websites | Incident | Abierta |
| HD-2 | No Internet Connection | Incident | Abierta |
| HD-3 | Printer Offline | Incident | Abierta |
| HD-4 | Disk Full / Low Disk Space Warning | Incident | Abierta |
| HD-5 | Access Denied to Shared Folder | Incident | Abierta |
| HD-6 | Password Reset Request | Service request | Esperando por ayuda |

## Estado del proyecto

En construcción. Se está validando primero la VM base y completando **HD-1** de principio a fin (inyección del fallo → ticket en Jira → grabación → troubleshooting → resolución → evidencia → cierre) antes de replicar el mismo proceso en el resto de tickets.
