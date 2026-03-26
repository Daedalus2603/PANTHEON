---
Proyect: "[[A.M.A.R.S.]]"
Type: Overview
Status: Active
---
# A.M.A.R.S.
###### Aplicación Multiplataforma de Administración Remota de Servidores
---

AMARS es una aplicación cliente-servidor diseñada para centralizar la gestión de múltiples servidores alojados en una misma máquina y administrarlos remotamente desde dispositivos móviles.
Esta herramienta permite administración de servidores de videojuegos de manera independiente y accesible desde dispositivos móviles, sin depender de infraestructura de terceros. Facilita el control de procesos, logs, backups, usuarios, roles, tickets y configuraciones, todo de forma remota. Está concebida para que sea escalable y modular.

### Principales funcionalidades
- Gestión de ciclo de vida de los servidores: iniciar, detener, estado.
- Monitorización básica de logs y backups.
- Administración de usuarios, roles y grupos.
- Sistema de tickets para soporte y administración.
- Arquitectura modular para distintos tipos de servidores y su implementación futura.

### Arquitectura conceptual
- Cliente móvil independiente.
- Backend modular con adaptadores para distintos tipos de servidores.
- Persistencia de datos y procesos

[[AMARS/Arquitectura|Arquitectura técnica]]
[[AMARS/Ideas|Objetivos a futuro]]

A.M.A.R.S forma parte del [[PANTHEON]] como un sistema independiente, capaz de operar de manera autónoma en cualquier entorno.  
Dentro de este ecosistema, es desarrollado y desplegado en [[APOLLO]] como entorno principal de pruebas y ejecución, sin que esto suponga una dependencia para su funcionamiento externo.  
En el futuro, podrá ser supervisado por [[HELIOS]].

DEV: The Architect.


