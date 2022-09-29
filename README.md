# Infraestructure as a Code (Iaac)
 Es un enfoque para la automatización de infraestructura basado en las practicas de desarrollo de software.

 ## Principios

- Los sistemas se pueden reproducir fácilmente
- Los sistemas son desechables
- Los sistemas son consistentes
- Los sistemas son repetibles
- El diseño siempre está cambiando

## Prácticas generales

- Utilizar archivos de definición
- Sistemas y procesos autodocumentados
- Versionar todas las cosas
- Preferir cambios pequeños
- Mantener los servicios continuamente disponibles

## Tipos de herramientas

1. ### Herramientas para definición de infraestructura

Permiten especificar **qué** recursos de infraestructura desean crear y **cómo** deben configurarse:

- Archivos de definición de configuraciones

2. ### Herramientas para configuración de servidores

Nos permite configurar la infraestructura con el estado deseado.

Diferentes enfoques para la gestión de servidores:

- Configuración de servidores
- Empaquetar plantillas de servidores
- Ejecutar comandos en los servidores
- Configuración desde un registro central

> **Aprovisionamiento** es el proceso que permite que un elemento esté listo para usar

## Factores a tomar en cuenta para elegir una herramienta

- Modo desatendido para herramientas de líneas de comando
- Idempotencia (n ejecuciones con el mismo resultado)
- Parametrizable

## Objetivos de la gestión automatizada de servidores

- Un nuevo servidor puede ser aprovisionado a demanda
- Un nuevo servidor puede ser aprovisionado sin intervención humana
- Cada cambio puede ser aplicado a un conjunto de servidores

## Herramientas

| Definición de infraestructura  | Configuración de servidores |
| ------------------------------ | --------------------------- |
| - Terraform                    | - Ansible                   |
| - Cloud formation (AWS)        | - Chef                      |
| - Open stack heat (Open Stack) | - Puppet                    |

## Soporte

| **App / Datos**    |
| ------------------ |
| **Dependencias** ✅ |
| **Infra** ✅        |

## Ventajas

|            |      |      |      |       |  ↗️   |         💻         |
| :--------: | :--: | :--: | :--: | :---: | :--: | :---------------: |
|     📜      |  ➡️   |  🐙   |  ➡️   |  🚰⚙️   |  ➡️   |         💻         |
|            |      |      |      |       |  ↘️   |         💻         |
| Definición |      | Git  |      | CI/CD |      | Aprovisionamiento |

**Parametrizable** Diferente por ambiente (dev, qa, prod)