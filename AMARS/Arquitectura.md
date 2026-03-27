---
Proyect: "[[A.M.A.R.S.]]"
Type: Architecture
---
# Arquitectura 
---

AMARS sigue una arquitectura de cliente-servidor donde:
- Un cliente móvil actúa como interfaz de usuario.
- Un backend central gestiona la lógica y control de servidores.
- La comunicación se realiza mediante una API expuesta por el backend.
- Los servidores gestionados se abstraen mediante adaptadores.

## Cliente
---
La arquitectura del cliente sigue un patrón MVVM, separando claramente la interfaz, la lógica de presentación y el acceso a datos. 

El cliente está compuesto por:
- Aplicación móvil (MAUI .NET8)
- Interfaz de usuario
- Comunicación con backend

#### Componentes
El frontend de AMARS se organiza en módulos según responsabilidades y componentes:
- Interfaces
	- Definición de estructuras de datos mediante interfaces enfocado en configuración del sistema y credenciales.
	- Garantiza consistencia en los datos manejados por la aplicación.
- Models
	- Definición de propiedades de clases.
	- Definición de datos para llamadas y recepciones de peticiones.
- Pages
	- Componentes gráficos.
	- Esqueleto del frontend.
- Popups
	- Componentes gráficos flotantes.
	- Reusables.
- Services
	- Lógica de negocio para las distintas llamadas a la API (Dividida por endpoints, heredando de una única clase con funcionalidad general).
	- Lógica de gestión de almacenamiento seguro.
	- Lógica de gestión de almacenamiento persistente para las configuraciones de la app.
- ViewModels
	- Lógica enlazada a los componentes gráficos.
	- Responsive.

## Servidor (MarsCore)
---
Backend principal de AMARS encargado de:
- API principal
- Lógica de negocio
- Sistema de autenticación
- Gestión de procesos
#### Componentes
El backend de AMARS se organiza en módulos según responsabilidades:
- Adapters 
	- Abstracción de distintos tipos de servidores de videojuegos mediante interfaz.
	- Implementaciones específicas con funciones comunes.
	- Permite desacoplar la lógica del sistema de implementaciones concretas.
- API
	- Punto de entrada del sistema.
	- Expone endpoints protegidos y gestiona peticiones.
- Core
	- Orquesta la lógica del sistema.
	- Coordina los distintos módulos.
- Data
	- Persistencia lógica en formato JSON  
	- Almacena estado del sistema (usuarios, tickets, servidores)
- Logs
	- Historial de entrada y salida de endpoints.
	- Sistema actualmente básico, con posibilidad de ampliación futura.
- Provisioner
	- Encargado de la creación y configuración de servidores.
	- Utiliza plantillas definidas en el módulo Servers.
	- Sigue un patrón similar a Adapters, pero orientado a la inicialización y la configuración.
- Servers
	- Almacén de plantillas que usa los Provisioners para crear la estructura inicial de cada servidor.
- Services
	- Implementación de lógica específica de negocio.
	- Ejecuta operaciones concretas.
- Storage
	- Gestión del acceso físico a datos  
	- Proporciona operaciones de lectura/escritura
- Config
	- Variables generales del entorno.
