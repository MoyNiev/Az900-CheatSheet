# Az900-CheatSheet

## Antes de comenzar.
En este archivo aprenderás los coneptos básicos para entender qué es y cómo funciona la nube "Azure" de Microsoft. Si hay algún concepto con el que no estés completamente familiarizado, prueba buscando en alguno de los dos glosarios.

### Glosarios.
* [Glosario general.](/Resources/General_glossary.md)
* [Glosario Azure.](/Resources/General_glossary.md)

## Introducción a la Nube.

### ¿Qué es la nube?
Este es un término que muchas veces hemos escuchado o utilizado, tal vez de manera errónea. La nube no es una entidad física o algo que podamos ver, es un conjunto de cosas. Una aproximación al concepto real es: un conjunto de servidores alrededor del mundo, interconectados para funcionar como una gran red de transferencia de información. Esta gran red de servidores se divide en regiones.
Los cables por los que se compone la red que es Internet se ven de la siguiente forma:

![](/Images/internet_cables.png)
Fuente: [NY Times](https://www.nytimes.com/interactive/2019/03/10/technology/internet-cables-oceans.html).

### ¿Qué es un servidor?
A un nivel muy básico, un servidor es un ordenador que pone sus recursos disponibles a través de la red.

## Introducción a los aspectos básicos de Azure.

### ¿Qué es Azure?
Azure es una plataforma de informática en la nube, que cuenta con más de 100 servicios para crear soluciones a las necesidades de sus clientes.

### ¿Qué es la informática en la nube?
La informática en la nube es la entrega de servicios informáticos que se encuentran en la nube, es decir en un servidor remoto al que se puede acceder a través de internet. Estos servicios se ofrecen en un sistema de pago por uso, es decir, solo necesitas pagar por el tiempo y por la catidad de recursos que utilizas.

### ¿Cómo funciona Azure?
Los recursos que se encuentran físicamente en los centros de datos de Azure se encuentran conectados mediante una capa de abstracción llamada "Hypervisor". Este Hypervisor emula todas las funciones de una computadorea real en una, o múltiples máquinas virtuales.Esta virtualización se repite de manera global en cada centro de datos que está distribuído de manera global. *Para tomar un recorrido virtual en un centro de datos haz clic [aquí](https://news.microsoft.com/stories/microsoft-datacenter-tour/).*
![](https://azurecomcdn.azureedge.net/cvt-55baaafaf70e68cbe2b3c8781f2be036eb84fad391931a39d455ac3b096774ab/images/shared/regions-map-desktop.svg)

En cada centro de datos tiene *mini racks*, llenos de servidores. Cada servidor incluye un *hypervisor* para correr múltiples máquinas virtuales. Todos los servidores se encuentran conectados mediante un *switch*. Un servidor en cada *rack* corre un software especial llamado *fabric controller*, cada *fabric controller* se encuentra conectado a un software especial llamado *orchestrator*. El *orchestrator* es el encargado de todo lo que sucede dentro de Azure, incluyendo las peticiones de los clientes. Un cliente puede hacer una petición a través de un *API* disponible en el [portal de Azure](https://portal.azure.com).

![](/Images/Azure.png)
