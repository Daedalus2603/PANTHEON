---
Proyect: "[[A.M.A.R.S.]]"
Type: Overview
Status: Active
---
# A.M.A.R.S.
###### Aplicación Multiplataforma de Administración Remota de Servidores

AMARS es una aplicación cliente-servidor diseñada para centralizar la gestión de multiples servidores alojados en una misma maquina y administrarlos remotamente desde dispositivos móviles.
Esta herramientas permite la gestión y administración de servidores de videojuegos de manera independiente y accesible desde dispositivos móviles, sin depender de infraestructura de terceros. Facilita el control de procesos, logs, back-ups, usuarios, roles, tickets y configuraciones, todo de forma remota. Esta concebida para que sea escalable y modular.

Principales funcionalidades:
- Gestión de ciclo de vida de los servidores: iniciar, detener, estado.
- Monitorización básica de logs y back-ups.
- Administración de usuarios, roles y grupos.
- Sistema de tickets para soporte y administración.
- Arquitectura modular para distintos tipos de servidores y su implementación futura.

Arquitectura conceptual:
- Cliente móvil independiente (interfaz MAUI).
- Backend modular (FLASK) con adaptadores para distintos tipos de servidores.
- Persistencia de datos

Objetivos a futuro:
- Consola en tiempo real
- Notificaciones nativas

