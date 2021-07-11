# Az900-CheatSheet

## Introducción a la Nube.

### ¿Qué es la nube?
Este es un término que muchas veces hemos escuchado o utilizado, tal vez de manera errónea. La nube no es una entidad física o algo que podamos ver, es un conjunto de cosas. Una aproximación al concepto real es: un conjunto de servidores alrededor del mundo, interconectados para funcionar como una gran red de transferencia de información. Esta gran red de servidores se divide en regiones.
Los cables por los que se compone la red que es Internet se ven de la siguiente forma:

![](/Images/internet_cables.png)
> Fuente: [NY Times](https://www.nytimes.com/interactive/2019/03/10/technology/internet-cables-oceans.html).

### ¿Qué es un servidor?
A un nivel muy básico, un servidor es un ordenador que pone sus recursos disponibles a través de la red.

## Introducción a los aspectos básicos de Azure.

### ¿Qué es Azure?
Azure es una plataforma de informática en la nube, que cuenta con más de 100 servicios para crear soluciones a las necesidades de sus clientes.

### ¿Qué es la informática en la nube?
La informática en la nube es la entrega de servicios informáticos que se encuentran en la nube, es decir en un servidor remoto al que se puede acceder a través de internet. Estos servicios se ofrecen en un sistema de pago por uso, es decir, solo necesitas pagar por el tiempo y por la catidad de recursos que utilizas.

### ¿Cómo funciona Azure?
Los recursos que se encuentran físicamente en los centros de datos de Azure se encuentran conectados mediante una capa de abstracción llamada "Hypervisor". Este Hypervisor emula todas las funciones de una computadorea real en una, o múltiples máquinas virtuales.Esta virtualización se repite de manera global en cada centro de datos que está distribuído de manera global. 
> *Para tomar un recorrido virtual en un centro de datos haz clic [aquí](https://news.microsoft.com/stories/microsoft-datacenter-tour/).*

![](https://azurecomcdn.azureedge.net/cvt-55baaafaf70e68cbe2b3c8781f2be036eb84fad391931a39d455ac3b096774ab/images/shared/regions-map-desktop.svg)

En cada centro de datos tiene *mini racks*, llenos de servidores. Cada servidor incluye un *hypervisor* para correr múltiples máquinas virtuales. Todos los servidores se encuentran conectados mediante un *switch*. Un servidor en cada *rack* corre un software especial llamado *fabric controller*, cada *fabric controller* se encuentra conectado a un software especial llamado *orchestrator*. El *orchestrator* es el encargado de todo lo que sucede dentro de Azure, incluyendo las peticiones de los clientes. Un cliente puede hacer una petición a través de un *API* disponible en el [portal de Azure](https://portal.azure.com).

![](/Images/Azure.png)

A nivel macro, es decir, más allá de los centros de datos. A nivel global Azure cuenta con más de 200 centros de datos, estos centros de datso se encuentran clasificados en diversas formas.
* **Región**: Una región es un área geográfica que cuenta con al menos un centro de datos. Las regiones influyen en el costo por uso de los servicios y en la disponibilidad de estos.
* **Geografía**: La geografía es un mercado que contiene dos o más regiones de Azure.
* **Zona de disponibilidad**: Una zona de disponibilidad consta de centros de datos separados físicamente dentro de una región. Si un centro de datos deja de funcionar dentro de una zona, habrá otro que siga funcionando, garantizando así la disponibilidad del servicio.
> *Para conocer más acerca de estos conceptos haz clic [aquí](https://docs.microsoft.com/es-mx/azure/availability-zones/az-overview).*

### Tipos de servicios.
En Azure existen tres tipos de servicios, los que definen el nivel de responsabilidad del cliente. Estos son:
* [**IaaS**](https://azure.microsoft.com/es-mx/overview/what-is-iaas/): La infraestructura como servicio es donde el cliente tiene una responsabilidad mayor. En este tipo de servicio solo se está alquilando la infraestructura, el usuario es responsable de administrarla.
* [**PaaS**](https://azure.microsoft.com/es-mx/overview/what-is-paas/): La plataforma como servicio representa un punto de responsabilidad media. En este servicio se alquila un lugar en la nube para desarrollar, concentrandonos en el desarrollo de nuestras aplicaciones y no en gestionar el servicio.
* [**SaaS**](https://azure.microsoft.com/es-mx/overview/what-is-saas/): En el software como servicio el cliente tiene la menor responsabilidad. Alquilando el software como servicio los usuarios simplemente se conectan y utilizan aplicaciones almacenadas en la nube.

### Tipos de productos.
Azure cuenta con más de 100 productos que ofrecen soluciones a sus clientes. Estos productos se pueden clasificar en 10 principales categorías que son:
1. **Proceso**: Este tipo de servicio son los más considerados al momento de decidirse en cambiar a Azure.
2. **Redes**: Para vincular recursos en los procesos y suministrar acceso a aplicaciones son las principales funciones de estos servicios.
3. **Almacenamiento**: Los servicios de almacenamiento nos permiten almacenar distintos tipos de archivos en la nube.
4. **Móvil**: Los desarrolladores pueden crear servicios de back-end móviles de forma rápida y sencilla. Facilitando la incorporación de características como inicio de sesión y la conexión con recursos locales como SQL Server.
5. **Bases de datos**: Azure proporciona diveros servicios de base de3 datos para almacenar gran variedad de volúmenes y tipos de datos. Con la conectividad global se puede acceder a estos datos al instante.
6. **Web**: Azure incluye soporte técnico de primera clase para compilar y hospedar aplicaciones web y servicios web basados en HTTP.
7. **IoT**: La capacidad de los dispositivos para obtener y luego retransmitir información para el análisis de los datos se conoce como IoT (internet de las cosas).
8. **Macrodatos**: las grandes cantidades de datos que requieren algunos sitemas requieren que se complique analizarlos, de forma que las técnicas tradiciones resultan deficientes. Azure admite una amplia gama de tecnologías y servicios para proporcionar soluciones de análisis y macrodatos.
9. **Inteligencia artificial**:  De la amplia gamas de servicios que componen la inteligencia artificial, el principal es el aprendizaje automático. El aprendizaje automático es una técnica que permite utilizar datos existentes para prever tendencias, resultados y comportamientos futuros. Mediante el aprendizaje automático, los equipos aprenden sin necesidad de programarlos explícitamente. 
10. **DevOps**: DevOps reúne a individuos, procesos y tecnología mediante la automatización de la entrega de software.

##Principales ventajas de usar Azure.

### Ventaja económica.

Para entender mejor esta ventaja es conveniente introducir dos conceptos muy importantes.
* **CapEx (capital expenditure)**: Es cuando una empresa invierte en equipo para montar una nube privada. Esto implica un alto costo inicial, costo que se deduce de impuestos. Una desventaja de esto es que se necesita una inversión considerable para escalar.
* **OpEx (operational expenditure)**: La empresa gasta en productos y servicios según sus necesidades. No se requiere un gasto inicial, el gasto se hace cada cierto periodo de tiempo e igualmente es deducible de impuestos.

Como podemos ver, Azure nos ofrece la ventaja de no hacer un gasto inicial; además de poder hacer uso de más recursos según nuestras necesidades, sin tener que hacer un gasto significativo.

### Alta disponibilidad.

Como aprendimos anteriormente, azure cuenta con regiones, esto nos permite poder optimizar el teimpo de respuesta dependiendo de la región que queramos utilizar. Además, Azure cuenta con zonas de disponibilidad, esto nos proporciona disponibilidad casi en todo momento: si un centro de datos deja de funcionar, podemos acceder a otro.

La disponibilidad de cada servicio depende de los acuerdos de nivel de servicio (SLA). Puedes consultar la disponibilidad de cada servicio haciendo clic [aquí](https://azure.microsoft.com/es-mx/support/legal/sla/).

### Escalabilidad.
La escalabilidad es obtener más recursos, con un cargo extra, dependiendo de nuestras necesidades. Esta se divide en dos:
* **Vertical**: La escalabilidad vertical consiste en agregar más recursos (como memoria ram, espacio de almacenamiento, capacidad de procesamiento, etc) a una máquina virtual según se requiera.
* **Horizontal**: La escalabilidad horizontal consiste en agregar más instancias de un recurso, como agregar más máquinas virtuales.
![Escalabilidad](/Images/Escalabilidad.png)

**Escalado automático**. En el escalado automático se aasignan recursos automáticamente, satisfaciendo los requerimientos.
> Para saber más acerca del escalado automático haz clic [aquí](https://docs.microsoft.com/es-mx/azure/architecture/best-practices/auto-scaling).
