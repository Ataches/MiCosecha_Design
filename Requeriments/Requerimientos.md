# Documento de requerimientos de software
## Mi cosecha 

- [Documento de requerimientos de software](#documento-de-requerimientos-de-software)
  * [Mi cosecha](#mi-cosecha)
  * [Propósito](#prop-sito)
  * [Alcance del software](#alcance-del-software)
  * [Funcionalidades del producto](#funcionalidades-del-producto)
  * [Clases y características de usuarios](#clases-y-caracter-sticas-de-usuarios)
  * [Requerimientos funcionales](#requerimientos-funcionales)
    + [Consultar datos históricos](#consultar-datos-hist-ricos)
      - [Descripción](#descripci-n)
        * [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado)
        * [Requerimientos funcionales](#requerimientos-funcionales-1)
    + [Graficar datos](#graficar-datos)
      - [Descripción](#descripci-n-1)
      - [Acciones y comportamiento esperado](#acciones-y-comportamiento-esperado)
      - [Requerimientos funcionales](#requerimientos-funcionales-2)
    + [Registrar usuario](#registrar-usuario)
      - [Descripción](#descripci-n-2)
      - [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado-1)
      - [Requerimientos funcionales](#requerimientos-funcionales-3)
    + [Iniciar sesión del usuario](#iniciar-sesi-n-del-usuario)
      - [Descripción](#descripci-n-3)
      - [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado-2)
      - [Requerimientos funcionales](#requerimientos-funcionales-4)
  * [Requerimientos no funcionales](#requerimientos-no-funcionales)
    + [Tiempo de espera](#tiempo-de-espera)
    + [Persistencia](#persistencia)
    + [Servicios web](#servicios-web)
    + [Fiabilidad](#fiabilidad)
    
## Propósito
Con el fin de aportar a la mejora de la administración de los productos agrícolas, se busca desarrollar un software para la administración (recomendación a la hora de siembra y manutención) de cultivos de arroz
en el departamento del Tolima.

## Alcance del software

El sistema muestra permite la visualización de graficas o la interacción con un chatbot para identificar factores que pueden influir en la producción de arroz del departamento de Tolima en el municipio de Saldaña.

## Funcionalidades del producto

Se incluye una lista de las principales funcionalidades, la información detallada de requerimientos funcionales se documenta en las secciones posteriores.

| Funcionalidad                                          | Requerimiento funcional                                  |
|--------------------------------------------------------|----------------------------------------------------------|
| Consultar datos históricos                             | Graficar temperatura maxima o minima                     |
|                                                        | Graficar brillo del sol                                  |
|                                                        | Graficar humedad relativa                                |
|                                                        | Graficar precipitación                                   |
| Graficar datos                                         | Obtener datos                                            |
| Registrar usuario                                      | Obtener datos                                            |
|                                                        | Registrar datos                                          |
| Iniciar sesión del usuario                             | Obtener datos                                            |
|                                                        | Consultar datos                                          |

## Clases y características de usuarios

| Usuario                                          | Característica                                |
|--------------------------------------------------|-----------------------------------------------|
| Usuario                                          | Interesado en la consulta de datos históricos relacionados con factores del clima que influyen con la producción de arroz |

## Requerimientos funcionales

### Consultar datos históricos

#### Descripción

Esta funcionalidad permite la consulta, visualización y redireccionamiento a los distintos tipos de gráficos y conjuntos de datos que tiene el sistema.

> __Prioridad__ alto

##### Acciones iniciadoras y comportamiento esperado

- Se espera que el sistema tenga la capacidad de redireccionar hacía el conjunto de datos solicitado por el usuario.
- Se espera que el sistema muestre la información de acuerdo a los datos de cada año.
- El usuario debe tener la capacidad de visualizar los datos ya sea por la interacción con el chatbot o por la interacción con el sistema.

##### Requerimientos funcionales

Para el siguiente listado de requerimientos funcionales se debe cumplir cada uno de los siguientes:

- El sistema debe permitir al usuario seleccionar tipo de las gráficas que desea visualizar.
- El sistema debe permitir al usuario seleccionar un año en específico de acuerdo a un conjunto de años que desea visualizar.

__REQ-1-F1__: Graficar temperatura maxima o minima

- El usuario debe tener la opción de seleccionar las gráficas relacionadas con la temperatura máxima o mínima en un año.

__REQ-2-F1__: Graficar brillo del sol

- El usuario debe tener la opción de seleccionar las gráficas relacionadas con la cantidad de brillo en un año.

__REQ-3-F1__: Graficar humedad relativa

- El usuario debe tener la opción de seleccionar las gráficas relacionadas con la humedad relativa en un año.

__REQ-4-F1__: Graficar precipitación

- El usuario debe tener la opción de seleccionar las gráficas relacionadas con las precipitaciones en un año.


### Graficar datos

#### Descripción

Con esta funcionalidad el sistema graficará a partir del análisis de los conjuntos de datos.

> __Prioridad__: alto

#### Acciones y comportamiento esperado
- El usuario o chatbot indicará al sistema las gráficas y datos que el usuario quiere visualizar.

#### Requerimientos funcionales

__REQ-1-F2__: Obtener datos

- A partir de un conjunto de datos en formato CSV el sistema obtendría la información necesaria para realizar las gráficas.

__REQ-2-F2__: Mostrar datos

- El sistema muestra el análisis realizado las gráficas permitiendo clasificar por distintos tipos de visualización, años y variables. 

### Registrar usuario

#### Descripción

Por medio de esta funcionalidad se busca dar la posibilidad al usuario registrarse dentro de la aplicación.

> __Prioridad__: medio

#### Acciones iniciadoras y comportamiento esperado
- El usuario inicia el sistema y no cuenta con una cuenta registrada.
- Sistema: Muestra las opciones para registrarse dentro de la plataforma y el usuario se registra.
- Sistema: Guarda los datos del usuario en la base de datos.

#### Requerimientos funcionales

__REQ-1-F3__: Obtener datos
- El sistema busca en la base de datos los usuarios registrados en la misma.

__REQ-2-F3__: Registrar datos
- El sistema validará las credenciales digitadas por el usuario.
- El sistema registra el usuario dentro de la base de datos. 

### Iniciar sesión del usuario

#### Descripción

Con esta funcionalidad el vendedor podrá visualizar los pedidos hechos por los clientes, el domiciliario podrá visualizar los pedidos a su nombre y el cliente podrá visualizar y/o validar el estado de su pedido (Recibido, en preparación, pago fallido, enviado, entregado, cancelado, no entregado).

> __Prioridad__: medio

#### Acciones iniciadoras y comportamiento esperado
- Usuario (cliente): Puede visualizar el estado actual de los pedidos realizados.
- Sistema: Muestra el estado de los pedidos al cliente.
- Usuario (vendedor): Logra visualizar los estados de los pedidos.
- Usuario (domiciliario): Logra visualizar los estados de los pedidos asignados para entrega o el histórico de pedidos entregados a su nombre.

#### Requerimientos funcionales

__REQ-1-F4__: Obtener datos
- El sistema busca en la base de datos los usuarios registrados en la misma.

__REQ-2-F4__: Consultar datos
- El sistema verifica que el usuario se haya registrado con las credenciales que utilizó.
- El sistema una vez validadas las credenciales redirige a la página principal de la plataforma.

## Requerimientos no funcionales

__REQNF-1__:
### Tiempo de espera

Para el funcionamiento de la aplicación se espera que el tiempo de respuesta sea imperceptible por el usuario final. Con este propósito, la aplicación considerada debe poseer un tiempo de respuesta menor o igual a 5 segundos.

- Criterios de aceptación:

La aplicación debe tener un tiempo de respuesta como máximo de 5 segundos en todas las tareas que tenga. De lo contrario, se considera que la aplicación no tiene el tiempo de respuesta menor o igual a 5 segundos.

__REQNF-2__:
### Persistencia

La información relacionada con el sistema debe ser manejada y almacenada mediante un gestor de base de datos relacional.

- Criterios de aceptación:
    - La información debe ser almacenada en distintas tablas que almacenen los datos.
    - La información debe ser manipulable a través de las diferentes operaciones del gestor de base de datos.

__REQNF-3__:
### Servicios web

La comunicación entre los componentes del sistema debe ser desarrollada con el uso de servicios web 

- Criterios de aceptación:
  - Hay comunicación entre componentes por medio de formatos de texto para el intercambio de datos como JSON

__REQNF-4__:
### Fiabilidad

El manejo de los datos dentro de la aplicación debe estar sujeto a exactitud y fiabilidad de la información ingresada al sistema y la proporcionada al el sistema.