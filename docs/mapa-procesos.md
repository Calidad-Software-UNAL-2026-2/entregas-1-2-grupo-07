# Mapa de Procesos Clave — EventMaster

> Generado automáticamente con el workflow de flujo único (modelo iterativo e incremental). La caracterización completa (estratégicos, de apoyo y clave) se documenta en la wiki (`03a-Mapa-Procesos-Caracterizacion`), y la definición formal del modelo de ciclo de vida en `04c-Modelo-Ciclo-Vida`.

## Proceso: Definición de Requisitos

- **Entradas:** Modelo verbal original de EventMaster, extensión del modelo verbal (`01-Extension-Modelo-Verbal`), retroalimentación de interesados.
- **Actividades:** Identificar actores, definir necesidades de negocio e interesados, especificar requisitos funcionales (historias de usuario con criterios de aceptación), requisitos no funcionales con métricas y requisitos de interfaz.
- **Salidas:** Actores (`02b`), Necesidades (`02c`, `02d`), Interfaces (`02e`), y línea base de 11 módulos, RF y RNF en GitHub Issues (vista Registro de Requisitos).
- **Recursos:** Guía BABOK v3, GitHub Wiki e Issues, sesiones de análisis del equipo.

## Proceso: Arquitectura y Diseño

- **Entradas:** Línea base de requisitos funcionales y no funcionales, requisitos de interfaz (`02e-Requisitos-Interfaz`) y restricciones tecnológicas (React y PostgreSQL).
- **Actividades:** Diseñar la arquitectura frontend-backend (API REST sobre HTTPS), modelar la base de datos en PostgreSQL, definir el esquema de almacenamiento local cifrado y sincronización *offline*, y diseñar prototipos de interfaz accesibles (WCAG 2.1).
- **Salidas:** Vistas arquitectónicas, modelo entidad-relación de PostgreSQL, especificación de endpoints API y prototipos UI/UX.
- **Recursos:** Herramientas de modelado y prototipado, especificaciones de React y PostgreSQL, pautas WCAG 2.1.

## Proceso: Implementación

- **Entradas:** Especificación de arquitectura y diseño, historias de usuario priorizadas por iteración y estándares de codificación.
- **Actividades:** Codificar interfaces en React, desarrollar lógica de negocio y APIs del backend, implementar persistencia en PostgreSQL, programar la carga diferida de banners y el módulo móvil de lectura QR *offline*, y ejecutar pruebas unitarias.
- **Salidas:** Componentes de software funcionales por módulo, migraciones de base de datos y resultados de pruebas unitarias.
- **Recursos:** Entorno de desarrollo (VS Code, Node.js, React, PostgreSQL), Git/GitHub, librerías de escaneo QR y cifrado.

## Proceso: Integración

- **Entradas:** Componentes de software implementados y probados unitariamente, especificación de interfaces externas (`02e-Requisitos-Interfaz`).
- **Actividades:** Ensamblar frontend React con el backend y PostgreSQL, conectar servicios externos (notificaciones, MFA, mapas y pagos), verificar la sincronización idempotente del padrón *offline* y ejecutar pruebas de integración.
- **Salidas:** Sistema EventMaster integrado en ambiente de pruebas y reporte de pruebas de integración.
- **Recursos:** Ambiente de integración/staging, APIs/sandboxes de servicios externos, herramientas de pruebas de API.

## Proceso: Verificación y Validación

- **Entradas:** Sistema integrado, criterios de aceptación de los 54 RF y umbrales de los 17 RNF (`[RNF-01]` a `[RNF-17]`).
- **Actividades:** Ejecutar pruebas funcionales de extremo a extremo, pruebas de carga y rendimiento (tiempos de respuesta y concurrencia), pruebas de seguridad (MFA y cifrado), validación de modo *offline* QR y pruebas de usabilidad (SUS ≥ 80) y accesibilidad (WCAG 2.1).
- **Salidas:** Reporte consolidado de pruebas, registro de defectos corregidos y acta de validación del prototipo funcional.
- **Recursos:** Plan y casos de prueba, herramientas de pruebas de rendimiento/carga, dispositivos móviles para pruebas de campo QR, encuestas SUS.

## Proceso: Transición

- **Entradas:** Prototipo funcional verificado y validado, manuales/guías de usuario y plan de despliegue.
- **Actividades:** Aprovisionar infraestructura productiva con alta disponibilidad (uptime ≥ 99.9%), desplegar aplicación y base de datos, configurar monitoreo de incidencias (MTTR < 24 h) y entregar la plataforma al cliente.
- **Salidas:** Plataforma EventMaster operando en producción, actas de entrega y canales activos de retroalimentación de usuarios.
- **Recursos:** Infraestructura cloud/hosting, scripts de despliegue, herramientas de monitoreo y alertas, documentación de usuario.

