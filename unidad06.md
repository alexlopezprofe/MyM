# Unidad 6. Dispositivos de almacenamiento

# Definición

Los dispositivos de almacenamiento de un equipo microinformático\, también conocidos como memoria secundaria\, es el lugar donde se almacenan permanentemente los programas y datos con los que se trabaja en el mismo\. Se caracteriza por tener gran capacidad de almacenamiento\, ser no volátil y por un tiempo de acceso más lento que el acceso a la memoria principal\.

![](assets%5Cimg%5CUnidad06%5CUnidad062.png)

# Unidad de almacenamiento principal

Actualmete los dispositivos de almacenamiento secundario principal en un equipo microinformático y donde se suele instalar el sistema operativo, además de tener la posibilidad de almacenar programas y datos son los **discos duros magnéticos o HDD (Hard Disk Drive)** y las **unidades de estado sólido o SDD (Solid State Drive)**

Sus características principales son:

+ Gran capacidad de almacenamiento\.
+ No volátil\.
+ Acceso más lento que la memoria principal(RAM)\.

![](assets%5Cimg%5CUnidad06%5CUnidad063.png)

![](assets%5Cimg%5CUnidad06%5CUnidad064.png)

![](assets%5Cimg%5CUnidad06%5CUnidad065.png)

## Disco duro magnético. Estructura mecánica

![](assets%5Cimg%5CUnidad06%5CUnidad066.png)

* Un disco duro magnético está formado por uno o varios  **discos** (o **platos**\)\, normalmente de aluminio\, que en su superficie se almacena la información ya que están recubiertos con un material **magnetizable**\.
* Estos platos están fijados en el centro a un eje donde hay un **motor de rotación** cuya misión es hacerlos girar al unísono a gran velocidad \(**rpm**\)\.
* Sobre los discos existen unos **brazos** encargados de moverse sobre toda la superficie del disco gracias a otro motor diferente\.
* En los extremos de estos brazos se instalan las **cabezas \(heads\)**   que son las que realizan las funciones de **lectura y escritura\**.
* Las cabezas se mueven a través de la superficie de los platos por la acción del **impulsor de cabeza**\.
* La **controladora** es una placa electrónica  encargada de sincronizar todas las acciones para conseguir la lectura/escritura\, y comunicarse con el resto del sistema a través del **interfaz**\.
* **Caché**\.  Las unidades actuales tienen un chip de memoria integrada en el circuito electrónico\. Éste hace las veces de puente de intercambio de información desde los platos físicos hasta la memoria RAM\.  Es como un búfer dinámico para aligerar el acceso a la información física y suele ser de 64 MB\.
* Todos los elementos anteriores se aglutinan en una **caja sellada**, para evitar la entrada de polvo y suciedad

### Disco o platos magnetizables

![](assets%5Cimg%5CUnidad06%5CUnidad067.png)

### Brazos

![](assets%5Cimg%5CUnidad06%5CUnidad068.png)

### Motor

![](assets%5Cimg%5CUnidad06%5CUnidad069.png)

El motor gira a una determinadas **RPM: revoluciones por minuto**

![](assets%5Cimg%5CUnidad06%5CUnidad0610.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0611.png)




### Cabezas

![](assets%5Cimg%5CUnidad06%5CUnidad0612.png)

### Cabezas lecto/escritoras

![](assets%5Cimg%5CUnidad06%5CUnidad0613.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0614.png)

### Controladora de disco

![](assets%5Cimg%5CUnidad06%5CUnidad0615.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0616.jpg)

## Estructura física

![](assets%5Cimg%5CUnidad06%5CUnidad0617.png)

* **Pistas\.** Son los distintos anillos concéntricos invisibles a lo largo de los cuales se graban los pulsos magnéticos\.
* **Sectores\.** Las distintas partes en las que se subdivide cada pista\. En el caso de los discos duros el número oscila entre los 15 y los 63 sectores\. El tamaño físico de un sector es de **512 bytes**\.
* **Cilindros\.** Es el conjunto de pistas a las que el SO puede acceder simultáneamente en cada posición de cabezas\. \(En el caso de un disco con dos platillos\, el cilindro constará de 4 pistas\)\. Así se accede más rápidamente al no tener que desplazar el cabezal\. En ocasiones se habla de número de cilindros por cara
* **Clúster\.** Conjunto contiguo de sectores que componen la unidad más pequeña de almacenamiento de un disco\. 
  > Los archivos se almacenan en uno o varios clústeres\, dependiendo de su tamaño\. 

  > En Windows &rarr; [Tamaño de asignación](https://www.xataka.com/basics/tamano-unidad-asignacion-disco-duro-que-cual-mejor-escoger)

Tamaño de la unidad de asignación en Windows →  Tamaño lógico del cluster

![](assets%5Cimg%5CUnidad06%5CUnidad0618.png)

[Tamaño predeterminado del tamaño de asignación en Windows](https://support.microsoft.com/es-es/topic/tama%C3%B1o-de-cl%C3%BAster-predeterminado-para-ntfs-fat-y-exfat-9772e6f1-e31a-00d7-e18f-73169155af95)

## Mecanismo de lectura/escritura

Los diferentes platos que forman el disco giran a una velocidad constante y no cesan mientras el disco duro está recibiendo energía\. Cada cara del plato tiene asignada una de las cabezas de lectura/escritura\. La cabeza se mueve desde el interior al exterior del plato\. Gracias a este movimiento de las cabezas y al giro de los platos se consigue acceder a todos los sectores\.

Los brazos que poseen las cabezas se mueven todos al unísono hacia el interior o exterior del plato\, como si fueran los dientes de un peine\. Por tanto\, todas las cabezas van a estar leyendo los sectores que forman el cilindro virtual\. De ahí que el proceso de lectura y escritura se haga al mismo tiempo en los sectores de cada pista que forma el cilindro\.

Las cabezas\, gracias al mismo aire que provoca el giro de los platos\, flotarán sobre la superficie de ellos\, siempre sin tocarla\. Cualquier mínimo contacto podría dañar la superficie y dejar el disco duro inutilizable\.

![](assets%5Cimg%5CUnidad06%5CUnidad0619.jpg)

### Geometría o direccionamiento de los HDD

Hace referencia al número físico real de cabezas\, cilindros\, pistas y sectores\. La capacidad del disco se puede calcular si se conocen estos valores\. Se distingue entre:

+ **CHS** (Cylinder Head Sector\)** \(cilindro cabeza sector\)\. Con estos tres valores se puede situar un sector cualquiera del disco\. → Es un método de direccionamiento obsoleto

+ **LBA (Logical Block Addressing)** \(direccionamiento lógico de bloques\)\, que consiste en dividir el disco entero en sectores y asignar a cada uno un único número\. Este es el que actualmente se usa\.

LBA0 representa el primer sector lógico del dispositivo

![](assets%5Cimg%5CUnidad06%5CUnidad0621.png)

La capacidad del disco se puede calcular si se conocen estos valores que normalmente podemos encontrar en la etiqueta de los discos\. El tamaño físico de un sector es de 512 bytes\.

![](assets%5Cimg%5CUnidad06%5CUnidad0622.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0623.png)

Capacidad\(CHS\)= C\*H\*S\*512B

Capacidad=19390\*16\*63\*512B=10\.007\.101\.440B style="color:#202124"> __≈  10GB

Capacidad \(LBA\)=Sectores\*512B

Capacidad=3907029168\*512B=2\.000\.398\.934\.016B style="color:#202124"> __≈  2TB

# 2.2 SSD.

SSD \(Solid   State   Drive \- Unidad de Estado Sólido\) utilizan un tipo de memoria flash NAND\.

Ventajas:

Rapidez\. Tanto en la búsqueda de los datos como en las lecturas posteriores\. En una unidad de este tipo el tiempo que tienes que esperar hasta obtener los datos es siempre el mismo \(similar a la RAM\)\. No es necesario desfragmentarlo\.

Mayor resistencia a golpes\. Al no tener componentes móviles responden mejor tanto a las vibraciones como a los golpes\.

Menor consumo de energía\. Necesitan menos potencia para funcionar\.

Menor ruido\. Otra ventaja más de no tener partes móviles\.

Inconvenientes:

Precio mayor\.

Menor capacidad\.

Menor tiempo de vida\.   

![](assets%5Cimg%5CUnidad06%5CUnidad0624.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0625.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0626.png)

# 2.2 SSD. Estructura interna

__Controlador \(__Controller__\):__  El controlador es el cerebro de la unidad SSD\. Se encarga de gestionar las operaciones de lectura y escritura\, así como de llevar a cabo la administración de la memoria\. Además\, controla la interfaz de conexión con la placa madre\, que suele ser SATA\, PCIe o NVMe\.

__Chips de memoria NAND Flash:__  La memoria NAND Flash es el componente fundamental de almacenamiento en una SSD\. Está compuesta por celdas de memoria que retienen los datos de forma no volátil\. Hay varios tipos de memoria NAND\.

__Cache DRAM__ : Algunas SSDs incorporan una memoria caché DRAM \(memoria de acceso aleatorio dinámica\) para mejorar el rendimiento\. Esta memoria se utiliza para almacenar temporalmente datos que se acceden con frecuencia\, acelerando las operaciones de lectura y escritura\.

__Conector:__  Las SSDs se conectan a la placa madre a través de un conector que puede ser SATA \(o mSATA\)\, NVMe o incluso PCI\-E\, dependiendo del modelo y la interfaz de conexión utilizada\.

__Firmware:__  El firmware es el software interno que reside en la SSD y es gestionado por el controlador\. Este software controla las operaciones\, la gestión de errores y las funciones avanzadas de la unidad SSD\.

![](assets%5Cimg%5CUnidad06%5CUnidad0627.jpg)

# 2.2 SSD. Tipos de conexión

![](assets%5Cimg%5CUnidad06%5CUnidad0628.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad0629.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad0630.jpg)

# 2.2 Disco duro SSD. Chips de Memoria NAND FLASH

<span style="color:#1E1E1E">Los chips de estas memorias basan su estructura en transistores de puerta flotante \(o transistores  style="color:#1E1E1E">floating style="color:#1E1E1E">\-gate\)\. La diferencia entre este tipo de transistores y los que usan la memoria DRAM\, es que estos últimos deben tener una carga eléctrica con una frecuencia de refresco constante para mantener los datos almacenados\. Este es el motivo por el que la memoria RAM de nuestro ordenador se vacía al apagar el ordenador\.

<span style="color:#1E1E1E">La memoria NAND está diseñada para mantener su estado de carga aun cuando no está recibiendo corriente eléctrica\, con lo que se consigue mantener la información\. Por lo tanto\, es un tipo de memoria no volátil

<span style="color:#1E1E1E">Los electrones son almacenados en el puente flotante \( style="color:#1E1E1E">Flaoting style="color:#1E1E1E"> Gate\)\, de forma que toma una lectura de 0 cuando está cargado\, o 1 si está vacío\. Son unos valores opuestos a lo que se suelen utilizar\. De ahí el nombre  style="color:#1E1E1E"> __N style="color:#1E1E1E">egated style="color:#1E1E1E">  style="color:#1E1E1E"> __AND

![](assets%5Cimg%5CUnidad06%5CUnidad0631.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad0632.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad0633.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad0634.jpg)

Los transistores que componen la memoria almacenan la información en   celdas   en las que se almacenan datos en forma de voltajes\. Dichas celdas forman matrices o   bloques   de las que a cada fila se le conoce como   página  ; 

![](assets%5Cimg%5CUnidad06%5CUnidad0635.png)

__¿En cada celda se almacena un bit?__

# 2.2 Disco duro SSD. Chips de Memoria

NAND SLC \(Single   Level   Cell\)   \-    _Ventaja: Mayor resistencia \- Desventaja: Cara y de baja capacidad_ 

La NAND SLC almacena 1 bit de información por celda\. La celda guarda un 0 o un 1 y\, en consecuencia\, los datos pueden escribirse y recuperarse más rápido\. SLC ofrece el mejor rendimiento y la mayor resistencia con 100\.000 ciclos de P/E \(  _[Ciclo de programación de borrado](https://uruguayoc.wordpress.com/2018/02/23/que-es-un-p-e-cycle-o-ciclo-de-programacion-borrado-de-una-celda-de-memoria-nand-flash/)_  \) por lo cual durará más que otros tipos de NAND\. Sin embargo\, por su baja densidad el SLC es el tipo de NAND más caro y\, por consiguiente\, no suele utilizarse en productos de consumo\. Normalmente se emplea en servidores y otras aplicaciones industriales que requieren rapidez y durabilidad\.

NAND MLC \(Multi   Level   Cell\)   \-    _Ventaja: Más barato que SLC \- Desventaja: Más lento y menos resistente que SLC_ 

La NAND MLD almacena 2 bits por celda \(00\, 01\, 10 y 11\)\, lo cual se traduce en poder almacenar el doble de información que un SLC en el mismo espacio\. Debido a esto MLC tiene una mayor densidad de datos que SLC y\, por consiguiente\, puede producirse con mayores capacidades\. MLC se caracteriza por una buena combinación de precio\, rendimiento y resistencia\. No obstante\, MLC es más sensible a errores de datos\, con 10\.000 ciclos de P/E por consiguiente\, su resistencia es inferior a SLC\. Normalmente\, MLC se utiliza en productos de consumo en los que la resistencia es menos importante\.

NAND TLC \(Triple   Level   Cell\)   \-    _Ventaja: Más barata y mayor capacidad \- Desventaja: Baja resistencia_ 

La NAND TLC \(celda de triple nivel\) guarda 3 bits por celda\, es decir\, hasta 8 estados diferentes\. Al agregarse más bits por celda\, el costo se reduce y la capacidad se incrementa\. No obstante\, esto tiene efectos negativos en el rendimiento y en la resistencia\, con solamente 3\.000 ciclos de P/E\. Muchos productos de consumo emplean TLC\, dado que es la opción más barata\.

# 2.2 Disco duro SSD. Memorias

NAND QLC

Cada celda almacena 4 bits\, lo que significa 16 estados de voltaje\.

![](assets%5Cimg%5CUnidad06%5CUnidad0636.png)

https://www\.profesionalreview\.com/2024/01/30/samsung\-memorias\-nand\-qlc\-280\-capas/

NAND 3D

Las celdas se apilan también verticalmente \(3D\) y no solo a lo largo y ancho \(2D\)\. Esto permite hacer las celdas más grandes y\, por lo tanto\, mejor aisladas\, minimizando los defectos de las memorias TLC considerablemente\, y acercándolas a las MLC en durabilidad\. La mayor densidad de memoria posibilita mayores capacidades de almacenamiento sin un enorme incremento de precio\. Por otra parte\, NAND 3D se caracteriza por su mayor resistencia y menor consumo eléctrico\.

![](assets%5Cimg%5CUnidad06%5CUnidad0637.png)

# 2.2 Disco duro SSD.

![](assets%5Cimg%5CUnidad06%5CUnidad0638.png)

# 3. Características generales disco duro

* Factor de forma:   El factor de forma nos da las dimensiones del disco duro\. Se mide en pulgadas\, las cuales indican el diámetro de los platos \(en el caso de que lleven\)\. Podemos encontrar los siguientes factores de forma
  * 3\,5 pulgadas\.
  * 2\,5 pulgadas\.
  * 1\,8 pulgadas\.
* Interfaz\. \(  Conexión al PC o dispositivo  \)\.   Podemos encontrar discos duros con la interfaz IDE\, SATA\, SCSI\, SAS o SATA Express\, pero también interfaces de conexión externos como USB\, Thunderbolt\, Firewire o eSATA\.
* Capacidad de almacenamiento\.   Se mide GB o TB
* Memoria caché\.   La memoria caché del disco duro almacenará la información más solicitada\, de manera que la controladora pueda acceder a ella de manera más rápida sin tener que ir a leerla internamente\. Esta memoria se mide en Megabytes\.
* Tiempo de acceso\.   El tiempo de acceso es el tiempo medio que tarda el disco duro en estar preparado para transferir datos \(ya sea de lectura o de escritura\)\. Este tiempo se mide en nanosegundos \(ns\)

![](assets%5Cimg%5CUnidad06%5CUnidad0639.png)

Temperatura\.   Indica el rango de temperaturas a las que el disco puede funcionar\.

Nivel sonoro:   Nos indica el nivel de ruido que emitirá el disco duro en funcionamiento\. Se mide en decibelios \(dB\)\.

Resistencia a golpes:   Mediría el golpe máximo que el disco duro es capaz de soportar sin romperse\. Se utiliza la medida de fuerza \(G\)\, donde 1G es la fuerza de la gravedad cuando estás parado\, sentado o acostado\.

Velocidad de rotación en   __discos duros magnéticos  \.   Marca la velocidad de giro en los discos duros magnéticos\. Los discos con interfaz IDE y SATA giran a 5\.400 o 7\.200 rpm \(revoluciones por minuto\)\. En los discos duros con interfaz SCSI o SAS las velocidades de giro son mayores\, de 10\.000 e incluso 15\.000 rpm\, aunque son ruidosos y consumen más energía\.

Velocidad lectura/escritura   __en discos SSD\.     Velocidad a la que el disco es capaz de leer y escribir información

Vida útil \- Terabytes Written \(TBW \)\.   Se define por el JEDEC como el número de terabytes que pueden ser escritos en un SSD hasta que sus células de memoria se «agoten»

Tiempo medio entre fallos \- Mean Time Between Failures \(MTBF\)    __en discos SSD\.

Humedad\.   Indica el rango de humedad a las que el disco puede funcionar\.

Altitud\.   Indica el rango de altitud  a las que el disco puede funcionar\.

…………\. 

…………\.

# 4. Interfaz IDE

I  DE \(Integrated Drive Electronics\)\,   ha sido la interfaz más utilizada hasta hace pocos años para la conexión de dispositivos de almacenamiento en los equipos microinformáticos\. Aunque actualmente no se fabrican dispositivos para esta interfaz\, es muy común encontrarnos equipos antiguos que la utilicen\.

![](assets%5Cimg%5CUnidad06%5CUnidad0640.png)

Cada conector IDE de la placa base  admite como máximo dos dispositivos IDE\, como por ejemplo dos discos duros\, o un disco y una unidad de DVD\-ROM o CD\. Uno se identificará como maestro \(master\) y otro como esclavo \(slave\)\. Para configurar un dispositivo IDE como maestro y esclavo se utilizan jumpers \(o puentes\) que se sitúan en la parte posterior del disco\.

La conexión de datos del dispositivo IDE a la placa base se hará mediante un cable plano que posee conectores de 40 pines

Para suministrar energía al dispositivo se utiliza el conector Molex que parte directamente de la fuente de alimentación\.

![](assets%5Cimg%5CUnidad06%5CUnidad0641.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0642.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0643.png)

# 4. Interfaz SATA

El interfaz SATA \(Serial Advanced Technology Attachment\)\,   es el sustituto de IDE para conectar dispositivos de almacenamiento en los equipos microinformáticos \(Discos duros/Unidades ópticas\)

Estándares:

![](assets%5Cimg%5CUnidad06%5CUnidad0644.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0645.png)

La velocidad de transferencia efectiva sólo tiene en cuenta los datos finales del usuario\, mientras que la velocidad de transferencia en bruto cuenta también los bits de control del interfaz \(bit de arranque y bit de parada\)\.

Los cables de datos solo poseen dos conectores\, uno en cada extremo\, por lo que sólo se podrá conectar un dispositivo SATA a cada uno de los conectores de la placa base\. Por tanto\, el concepto de maestro y esclavo desaparece en esta interfaz\. El conector de datos tiene un ancho de 1 mm y está compuesto de 7 hilos\. 

Conector de alimentación SATA directo desde la fuente\.

![](assets%5Cimg%5CUnidad06%5CUnidad0646.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0647.png)

# 4. Interfaz NVMe - M.2

NVMe son las siglas de «Non\-Volatile Memory Express»\, o memoria exprés no volátil\.

Utiliza la tecnología PCI\-Express lo que le permite al disco duro ofrecer un ancho de banda mucho más amplio en   _[comparación con la interfaz SATA\.](https://www.geeknetic.es/Guia/2189/SSD-M2-NVMe-y-SATA-Caracteristicas-y-Diferencias.html)_

![](assets%5Cimg%5CUnidad06%5CUnidad0648.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0649.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0650.png)

# 4. Interfaz SCSI

![](assets%5Cimg%5CUnidad06%5CUnidad0651.png)

 __La interfaz SCSI \(Small Computers System Interface \- Interfaz de Sistema para Pequeñas Computadoras\)\.   Todo lo contrario a lo que su nombre indica\, se utilizaba en entorno profesionales\. 

Los discos duros de esta interfaz son más caros y suelen ser más rápidos a la hora de transmitir datos ya que usan menos el microprocesador para esa tarea\. 

Actualmente este interfaz está obsoleto\, y ha dado paso a su sucesor SAS\.

Utiliza el modo de transmisión paralelo y permite la conexión de hasta 16 dispositivos\, incluida la controladora\.

Las placas bases no solían disponer de conectores SCSI integrados\, por lo que se necesitaba una tarjeta de expansión SCSI adicional para poder conectarlos\.

# 4. Interfaz SAS

El interfaz SAS \(Serial Attached SCSI\) es una interfaz de conexión de dispositivos de almacenamiento que ha sido la sucesora del interfaz SCSI\. → Servidores

Aumenta la velocidad de transferencia al aumentar el número de dispositivos conectados\, hasta 128 dispositivos

![](assets%5Cimg%5CUnidad06%5CUnidad0652.png)

Las placas base no suelen tener este tipo de controladoras integradas\, necesitando tarjetas de expansión adicionales para poder utilizar este tipo de interfaz\.

Similar al conector de la interfaz SATA\, pero el conector del disco duro posee una particularidad\, el conector de datos y el de alimentación están unidos sin separación entre ellos\. Debido a esta particularidad\, los discos duros SATA pueden ser utilizados en una controladoras SAS\, pero no a la inversa

![](assets%5Cimg%5CUnidad06%5CUnidad0653.png)

# 5. Discos duros externos

USB

Thunderbolt 

eSATA

![](assets%5Cimg%5CUnidad06%5CUnidad0654.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0655.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0656.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0657.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0658.png)

# 6. Factor de forma

![](assets%5Cimg%5CUnidad06%5CUnidad0659.png)

# 6. Factor de forma 3,5”

Son los discos duros usados comúnmente en los ordenadores de sobremesa\.

Discos duros actuales →  Interfaz SATA / SAS

Medidas típicas de 101 x 25\,4 x 146   mm\.

![](assets%5Cimg%5CUnidad06%5CUnidad0660.png)

<span style="color:#202124">Suelen tener unas dimensiones de 6\,9 x 10 x 9\,7 centímetros

<span style="color:#212529">Podemos encontrar discos de 2\.5” tanta magnéticos como SSD\.

<span style="color:#212529">Actualmente → Interfaz SATA\.

![](assets%5Cimg%5CUnidad06%5CUnidad0661.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0662.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0663.png)

# 6. Factor de forma 1.8”

<span style="color:#212529">Hay que distinguir entre discos con factor de forma 1\.8” con conexión mSATA y conexión  style="color:#212529"> _PCI\-Express \(NVMe M\.2\)_ 

![](assets%5Cimg%5CUnidad06%5CUnidad0664.png)

<span style="color:#666666">Arriba disco mSATA\, Abajo disco M\.2\.

# 6. NVMe M.2

<span style="color:#212529">El formato M\.2 se ha convertido en el más popular para la construcción de discos SSD de altas prestaciones\, pues permite la construcción de modelos muy rápidos\, con una alta capacidad y con un tamaño muy reducido\.

<span style="color:#212529">Se conectan mediante tecnología PCI\-Express a la placa base para evitar los cuellos de botella\.

<span style="color:#212529">Se elimina el conector de la alimentación\, pues los M\.2 se alimentan directamente desde la ranura PCI Express X4\. \(Actualmente existe PCI Express V5\)

<span style="color:#212529">Dentro del formato M\.2 existen varios tipos\, por ejemplo M\.2 2242\, M\.2 2260 y M\.2 2280\, esto hace referencia a las dimensiones del dispositivo\, en el primer caso son 22 mm de ancho x 42 mm de largo mientras que en el segundo tiene un largo de 60 mm y el último un largo de 80 mm\.

![](assets%5Cimg%5CUnidad06%5CUnidad0665.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0666.png)

# 7. Almacenamiento en red. NAS

<span style="color:#212529">El almacenamiento conectado en red\, Network Attached Storage \(NAS\)\, es el nombre dado a una tecnología de almacenamiento dedicada a compartir la capacidad de almacenamiento de un computador/ordenador \(servidor\) con computadoras personales o servidores clientes a través de una red \(normalmente TCP/IP\)\, haciendo uso de un sistema operativo optimizado para dar acceso con los protocolos CIFS\, NFS\, FTP o TFTP\. 

<span style="color:#212529">Suelen tener varios discos y se  pueden configurar en   _[RAID](https://es.wikipedia.org/wiki/RAID)_

<span style="color:#212529">Hay discos duros exclusivos para NAS que tienen más durabilidad\, los discos utilizados suelen ser magnéticos de 3\,5”

![](assets%5Cimg%5CUnidad06%5CUnidad0667.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0668.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0669.png)

# 7. Almacenamiento en red. Cabina de discos

![](assets%5Cimg%5CUnidad06%5CUnidad0670.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0671.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0672.png)

_[https://www1\.la\.dell\.com/ue/es/gen/Empresarial/pvaul\_md1000/pd\.aspx?refid=pvaul\_md1000&s=gen](https://www1.la.dell.com/ue/es/gen/Empresarial/pvaul_md1000/pd.aspx?refid=pvaul_md1000&s=gen)_   

# 8. RAID

<span style="color:#212529">Un RAID es un grupo de discos duros independientes configurados para funcionar como uno solo\, ya sea sumando su espacio total\, mejorando la velocidad de lectura y escritura o configurados para duplicar la información para estar seguros de que\, en caso de que uno de los discos duros se rompa\, no vamos a perder los datos\.

<span style="color:#212529">Existen varios tipo de RAID

![](assets%5Cimg%5CUnidad06%5CUnidad0673.png)

# 8.1. RAID 0

<span style="color:#333333"> __RAID 0 style="color:#333333">\. En esta configuración todos los discos duros funcionan como un único volumen\, y su espacio total es la suma del espacio de todos los discos duros\.

<span style="color:#333333">Doble velocidad de lectura y escritura\.

<span style="color:#333333">No hay paridad de datos ni volumen de respaldo\.

![](assets%5Cimg%5CUnidad06%5CUnidad0674.png)

# 8.2 RAID 1

<span style="color:#333333"> __RAID 1  style="color:#333333">es uno de los tipos de RAID más utilizados para quienes buscan duplicidad de los datos para estar seguros de que los datos nunca se pierden\. En este tipo de RAID\, los datos se duplican en los discos duros como si fuese un espejo\.

<span style="color:#333333">Mayor velocidad de lectura\. Sin mejora en la velocidad de escritura\.

<span style="color:#333333">Un disco duro espejo\. Si falla uno de los discos duros se puede reemplazar sin perder datos\.

<span style="color:#333333">Perdemos el 50% del espacio total de los discos\. El espacio total de un RAID 1 es la mitad del espacio total de los discos duros\. Por ejemplo\, si hacemos un RAID 1 con dos discos duros de 4 TB solo tendremos un espacio total de 4 TB\.

![](assets%5Cimg%5CUnidad06%5CUnidad0675.png)

# 8.3. RAID 5

<span style="color:#333333"> __RAID 5\, style="color:#333333"> la información se distribuye a lo largo de todos los discos duros\, aunque se reserva dicho espacio \(el tamaño de una de las unidades\) para paridad\. Esta paridad\, además\, se reparte entre todos los discos duros\.

<span style="color:#333333">Si fallan dos discos se pierde absolutamente toda la información del RAID\.

<span style="color:#333333">La mejora de velocidad de lectura es también X\-1 veces el número de discos usados\. 

<span style="color:#333333">El espacio total de los discos es X\-1\, El espacio total de un RAID 5 es el espacio de todos los discos duros menos 1\, es decir\, si vamos a usar 4 discos duros de 4 TB el espacio total será de 12 TB\.

<span style="color:#333333">Si falla uno de los discos duros\, cualquiera de ellos\, se puede reemplazar y recuperar todos los datos\.

![](assets%5Cimg%5CUnidad06%5CUnidad0676.png)

# 8.4. RAID 6

<span style="color:#333333"> __RAID 6\,  style="color:#333333">Prácticamente igual que el RAID 5\, pero añade un segundo nivel de paridad\, lo que nos permite que fallen hasta dos discos duros del RAID y poder sustituirlos\. Si fallan 3\, entonces toda la información del RAID se pierde\.

<span style="color:#333333">El espacio total de los discos es X\-2\, igual que la mejora de la velocidad de lectura\. A cambio de esta doble paridad incluida en el RAID 6 se pierde el espacio total de dos de los discos duros\. Por ejemplo\, en una configuración de 4 discos duros de 4 TB\, el espacio total que tendríamos es de 8 TB\, con el doble de velocidad de lectura\.

![](assets%5Cimg%5CUnidad06%5CUnidad0677.png)

# 9. Almacenamiento en la nube

![](assets%5Cimg%5CUnidad06%5CUnidad0678.png)

* <span style="color:#212529">Un sistema de almacenamiento en la nube o Cloud Storage es un modelo de almacenamiento de datos basado en redes de ordenadores donde nuestros datos están alojados en espacios de almacenamiento virtualizados\. Por lo tanto\, el espacio no se encuentra en el propio equipo físico del usuario\, sino en uno o varios servidores ofrecidos por la compañía que contratemos el servicio\. 
* <span style="color:#212529">Tipos:
* <span style="color:#212529"> __Público:  style="color:#212529">Ofrece recursos informáticos de un proveedor externo compartidos entre varias organizaciones o «clientes»\, lo que permite reducir los costes y el mantenimiento y facilitar la escalabilidad\. La gestión de la infraestructura la realiza el proveedor
  * <span style="color:#212529">Microsoft Azure\, AWS\, Google Cloud\, 
* <span style="color:#212529"> __Privados style="color:#212529">\. La infraestructura y los servicios se alojan en el centro de datos propio de una empresa\, garantiza un mayor control sobre los datos y más seguridad\. Las empresas o los usuarios los que tienen el control administrativo y tienen la posibilidad de diseñar y configurar el sistema en base a sus necesidades\.
  * <span style="color:#212529">CA Technologies\, Cisco\, Dell\, Egenera\, EMC\, HotLink\, Hewlett Packard Enterprise\, IBM\, Joyent\, Microsoft\, Mirantis\, OpenStack\, Oracle\, Rackspace\, Red Hat\, RightScale\, VMware
* <span style="color:#212529"> __Híbridos\, style="color:#212529"> son una combinación de los sistemas de almacenamiento públicos y privados\. De esta manera\, los datos más importantes se pueden guardar en una nube privada\, mientras que la información menos importante se almacena en un servicio de almacenamiento en la nube público\.

# 10. Memorias Flash

<span style="color:#333333">Es una memoria de tipo EEPROM \(Electrically\-Erasable Programmable Read\-Only Memory\)\.

<span style="color:#333333">Características

<span style="color:#333333">Gran resistencia a los golpes\.

<span style="color:#333333">Bajo consumo\.

<span style="color:#333333">Silencioso\, \(no contiene partes móviles\)\.

<span style="color:#333333">Pequeño tamaño y ligereza\.

<span style="color:#333333">Gran versatilidad \(cámaras digitales\, teléfonos móviles\, etc\.\)

<span style="color:#333333">Formatos:

<span style="color:#333333"> __Secure Digital \(SD\)

<span style="color:#333333"> __Pendrive \(memorias USB\)

<span style="color:#333333">CompactFlash \(CF\)

<span style="color:#333333">SmartMedia Card \(SMC\)

<span style="color:#333333">Memory Stick \(MS\)

<span style="color:#333333">Multimedia Card o MMC\.

<span style="color:#333333">xD\-Picture Card \(xD\)

![](assets%5Cimg%5CUnidad06%5CUnidad0679.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0680.png)

# 10.1 Memorias Flash SD

<span style="color:#333333">Secure Digital \(SD\) es un formato de tarjeta de memoria para dispositivos portátiles\, cámaras digitales \(fotográficas o video\)\, teléfonos móviles\, ordenadores portátiles etc\.\. 

<span style="color:#2C2C2C">SD Association \-   _[https://www\.sdcard\.org/](https://www.sdcard.org/)_ style="color:#333333"> 

<span style="color:#333333"> __Versiones:

<span style="color:#333333">SDSC:  Standard Capacity \-  hasta 2 GB de datos\.

<span style="color:#333333">SDHC: High Capacity \- hasta 32 GB de datos\.

<span style="color:#333333">SDXC: Extended Capacity \- hasta 2 TB de datos

<span style="color:#333333">SDUC: Ultra Capacity \- hasta 128TB

<span style="color:#333333"> __Factor de forma: style="color:#333333"> 

<span style="color:#333333">SD\, miniSD\, microSD\.

![](assets%5Cimg%5CUnidad06%5CUnidad0681.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0682.png)

<span style="color:#333333">Las tarjetas SD también se diferencian entre ellas mediante su clase \(velocidad\)

<span style="color:#333333"> __Clase 2:  style="color:#333333">Tienen una velocidad de escritura mínima de 2 MB/s\, y pueden ser usadas para hacer fotos y grabar vídeos en baja resolución\.

<span style="color:#333333"> __Clase 4:  style="color:#333333">Tienen una velocidad de escritura mínima de 4 MB/s\, y pueden ser usadas para grabar vídeos en HD de 720p\.

<span style="color:#333333"> __Clase 6: style="color:#333333"> Tienen una velocidad de escritura mínima de 6 MB/s\, y pueden ser usadas para grabar vídeos en HD de 720p\.

<span style="color:#333333"> __Clase 10: style="color:#333333"> Tienen una velocidad de escritura mínima de 10 MB/s\, y pueden ser usadas para sacar fotos de alta definición consecutivas y grabar vídeos en FullHD de 1080p o resoluciones inferiores\.

<span style="color:#333333"> __UHS Speed Class 1 \(U1\): style="color:#333333"> Tienen una velocidad de escritura mínima de 10 MB/s\, pero como tiene un bus mejor que la Clase 10 es mejor para grabar vídeos FullHD a 1080p que son más pesados\.

<span style="color:#333333"> __UHS Speed Class 3 \(U3\): style="color:#333333"> Tienen una velocidad de escritura mínima de 30 MB/s\, y es la más indicada para grabar vídeos en resoluciones 4K\.

![](assets%5Cimg%5CUnidad06%5CUnidad0683.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0684.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0685.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0686.png)

<span style="color:#333333">Las tarjetas SD también pueden diferenciarse por su clase para grabación de vídeo:

<span style="color:#333333"> __Clase V6 style="color:#333333">: Está en las tarjetas de Clase 6\, para la grabación de vídeo HD a 720p\.

<span style="color:#333333"> __Clase V10:  style="color:#333333">Está en las tarjetas de Clase 10 y UHS1\, para sacar fotos de alta definición consecutivas y grabar vídeos en FullHD de 1080p o resoluciones inferiores

<span style="color:#333333"> __Clase V30: style="color:#333333"> En las tarjetas de Clase U3\, para vídeos 4K a 24/30 fps

<span style="color:#333333"> __Clase V60: style="color:#333333"> En las tarjetas de Clase U3\, para vídeos 4K a 60/120 fps

<span style="color:#333333"> __Clase V90: style="color:#333333"> En las tarjetas de Clase U3\, para vídeos 8K a 60/120 fps

![](assets%5Cimg%5CUnidad06%5CUnidad0687.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0688.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0689.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0690.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0691.png)

# 10.2 Memorias Flash. Pendrive

<span style="color:#333333">Unidad de almacenamiento de datos que puedes conectar a ordenadores u otros dispositivos electrónicos\, desde móviles hasta televisores o consolas\, mediante su conector USB \(Clase A o clase C\)\, de ahí que se le conozca también como memoria USB\.

<span style="color:#333333">Sus capacidades y velocidades de transmisión de datos dependen de cada uno de los modelos\, ya que cada fabricante ofrece diferentes tamaños\, y con el paso del tiempo las velocidades han ido aumentando\.

<span style="color:#333333">Aquí\, el almacenamiento de cada pendrive lo puedes formatear con diferentes tipos de   _[sistema de archivos](https://www.xataka.com/basics/megaguia-formatos-que-sistema-archivos-formatear-usb-disco-duro-uso-que-vas-a-darle)_ style="color:#333333">\,

![](assets%5Cimg%5CUnidad06%5CUnidad0692.png)

<span style="color:#333333">Usos:

<span style="color:#333333">Llevar documentos o archivos multimedia para leerlos en cualquier ordenador u otro dispositivo

<span style="color:#333333">Guardar copias de seguridad\.

<span style="color:#333333">Crear un USB booteable\, que puede servir para reparar tu sistema operativo o para instalar otro sistema operativo en el ordenador

<span style="color:#333333">Utilizar el pendrive como llave de seguridad\, que sirve para verificar tu identidad en procesos de identificación en dos pasos\.

![](assets%5Cimg%5CUnidad06%5CUnidad0693.png)

# 11. Unidades ópticas

<span style="color:#333333">Las unidades de almacenamiento óptico son  aquellas que son capaces de leer y escribir datos por medio de un rayo láser en un soporte óptico\, ya que se almacenan por medio de ranuras microscópicas quemadas\. La información queda grabada en la superficie de manera física\, por lo que solo el calor \(puede producir deformaciones en la superficie del disco\) y las ralladuras pueden producir la pérdida de los datos\, en cambio es inmune a los campos magnéticos y la humedad\.

<span style="color:#333333">Los discos compactos \(CD\)\, discos versátiles digitales \(DVD\) y discos Blu\-ray \(BD\) son los tipos de medios ópticos más comunes que pueden ser leídos y grabados por estas unidades\.

![](assets%5Cimg%5CUnidad06%5CUnidad0694.png)

# 11.1 CD-ROM

![](assets%5Cimg%5CUnidad06%5CUnidad0695.png)

* <span style="color:#333333">El CD\-ROM \( style="color:#202124">Compact Disc Read\-Only Memory style="color:#333333">\) estándar fue establecido en 1985 por Sony y Philips\. 
* <span style="color:#333333">Actualmente en desuso al menos en los equipos microinformáticos
* <span style="color:#333333">Conexiones: IDE\-SATA o externos
* <span style="color:#333333">Puede albergar 650 \( style="color:#333333">74 minutos de música style="color:#333333">\) o 700 MB de datos \(80 minutos de música\) y los especiales de gran capacidad pueden llegar a los 800 y 900 MB\.
* <span style="color:#333333">Existen los siguientes formatos:
  * <span style="color:#333333">CD\-ROM \(CD Read Only Memory\)
  * <span style="color:#333333">CD\-DA \(Compact Disk Digital Audio\)
  * <span style="color:#333333">CD\-R \(CD Recordable\)
  * <span style="color:#333333">CD\-RW \(CD Rewritable\)
* <span style="color:#202122">Un CD de audio se reproduce a una velocidad tal que se leen 150 __[KB](https://es.wikipedia.org/wiki/Kilobyte)__ por segundo\. Esta velocidad base se usa como referencia para identificar otros lectores como los de __[ordenador](https://es.wikipedia.org/wiki/Computadora_electr%C3%B3nica)__\, de modo que si un lector indica 24x\, significa que puede llegar a leer hasta 24 x 150 KB/S = 3\.600 KB/__[s](https://es.wikipedia.org/wiki/Segundo)__

![](assets%5Cimg%5CUnidad06%5CUnidad0696.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0697.png)

Velocidad de lectura/escritura CD CAV \(Constant Angular Velocity\)

Si un lector indica 24x\, significa que puede llegar a leer hasta:

Velocidad = 24 x 150 KB = 3\.600 KB/s

![](assets%5Cimg%5CUnidad06%5CUnidad0698.png)

![](assets%5Cimg%5CUnidad06%5CUnidad0699.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06100.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06101.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06102.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06103.png)

# 11.2 DVD

![](assets%5Cimg%5CUnidad06%5CUnidad06104.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06105.png)

* Digital Versatile Disc \(disco versátil digital\)
* 1995→ style="color:#202122"> _DVD Consortium_ 
* Un DVD puede tener  dos capas y dos caras\, su capacidad va de 4\,7 GB a 17 GB
* Pueden leer y escribir\* también CDs
* La velocidad de transferencia de datos de una unidad DVD está dada en múltiplos de 1350 KB/s
* Existen los siguientes formatos:
  * DVD\-ROM
  * DVD\-Vídeo
  * DVD\-Audio
  * DVD\-R \(recordable\) / DVD\+R
  * DVD\-RW \(rewritable\) / DVD\+RW
  * DVD\-R DL \(dual layer\) / DVD\+R DL
* \.

![](assets%5Cimg%5CUnidad06%5CUnidad06106.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06107.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06108.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06109.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06110.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06111.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06112.png)

# 11.3 Blu-Ray

* <span style="color:#333333">La tecnología Blu\-Ray \(https://us\.blu\-raydisc\.com/\) hace uso de un rayo láser de color  style="color:#0000FF">azul  style="color:#333333">con una longitud de onda de 405 nanómetros\.  style="color:#0645AD"> _[¿Por qué es azul?](https://www.adslzone.net/2017/10/30/por-que-laser-blu-ray-azul/)_ 
* <span style="color:#333333">Desarrollado por la Blu\-ray Disc Association \(BDA\) \(2002\)
* <span style="color:#333333">La capacidad del Blu\-ray es de 25 GB para una capa\, 50 GB para doble capa \, 100 GB para triple capa y 128 GB para cuádruple capa \(BD\-XL\)
* <span style="color:#333333">Los usos principales del Blu\-ray son la grabación y\, la distribución del vídeo de alta definición\, el almacenamiento de datos y la gestión de activos digitales\. Por otro lado\, uno de los usos más recurrentes son los videojuegos
* <span style="color:#333333">Existen los siguientes formatos:
  * <span style="color:#333333">BD\-ROM
  * <span style="color:#333333">BD\-R \(recordable\)
  * <span style="color:#333333">BD\-RE \(rewritable\)
* <span style="color:#333333">La velocidad de transferencia va a venir expresada por un número seguido de una “X”\. En este caso la “X” se refiere a una velocidad de 4\,5MB/s\. Actualmente existen unidades lectoras de BD con una velocidad de 12x\.
* <span style="color:#333333">Pueden leer y escribir\* también CD y DVD

![](assets%5Cimg%5CUnidad06%5CUnidad06113.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06114.png)

# 11. Unidades ópticas

![](assets%5Cimg%5CUnidad06%5CUnidad06115.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad06116.jpg)

# 12. Cintas magnéticas

<span style="color:#333333">Las cintas magnéticas de almacenamiento de datos han sido usadas para el almacenamiento de datos durante los últimos 50 años\.

<span style="color:#333333">Las cintas magnéticas son un tipo de medio o soporte de almacenamiento de datos que se graba en pistas sobre una banda plástica con un material magnetizado\.

<span style="color:#333333">Se mantienen como una alternativa a los discos debido a su bajo coste por bit\. 

<span style="color:#333333">Se utilizan para copias de seguridad\.

<span style="color:#333333">La grabación y lectura se efectúan de forma secuencial\, que significa que para encontrar algo que está en medio de la cinta debes “hacerla avanzar” previamente hasta que el cabezal de lectoescritura se posicione sobre el lugar correcto\, proceso que puede demorar varios minutos

![](assets%5Cimg%5CUnidad06%5CUnidad06117.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06118.png)

# 12. Cintas magnéticas.LTO

<span style="color:#333333"> __Linear Tape\-Open \(LTO\)  style="color:#333333">es una tecnología de cinta magnética de almacenamiento de datos\, desarrollada originalmente a finales de 1990\.

![](assets%5Cimg%5CUnidad06%5CUnidad06119.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06120.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06121.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06122.jpg)

![](assets%5Cimg%5CUnidad06%5CUnidad06123.jpg)

# 13. Estructura lógica de los discos

La estructura de partición  \. Se encarga de definir cómo se organiza la información en el disco duro\. Independientemente del hardware o del sistema operativo\, todas las computadoras se inician utilizando   MBR \(BIOS\)   o   GPT \(UEFI\)  \. 

Espacio particionado  \. Es el espacio del disco que ha sido asignado a alguna partición\.  Una partición es una división del disco duro\, de forma que el sistema operativo la considera como si fuera una unidad totalmente independiente\. Algunos usuarios prefieren tener particiones independientes para los datos personales\, los programas y los archivos del sistema operativo\.

Espacio sin particionar\.   Es espacio no accesible del disco ya que todavía no ha sido asignado a ninguna partición y está sin formatear\.

# 13. MBR (Master Boot Record)

* <span style="color:#333333">En discos duros que tienen tabla de particiones con el esquema MBR\, cuando se crean las particiones\, se graba dicha información en el sector de arranque del disco \(MBR\)\. Básicamente\, el MBR es un tipo especial de sector de arranque que se encuentra en el comienzo de los dispositivos de almacenamiento de datos particionados\, como un disco duro fijo o una unidad de almacenamiento externa\, y que contiene una tabla de particiones que indica el lugar del disco donde se encuentran las particiones\. Normalmente\, en dicha tabla se guarda información sobre:
  * <span style="color:#333333">el tipo de partición\,
  * <span style="color:#333333">el tamaño de la partición \(se indica dónde empieza y dónde acaba cada partición\)\,
  * <span style="color:#333333">si es o no la partición activa \(que es la que está configurada para arrancar\)\.
* <span style="color:#333333">De esta forma\, cuando arranca un ordenador la BIOS intenta localizar el MBR donde identifica la partición definida como activa y se inicia el proceso de arranque\. Dicho de otra forma\, el MBR apunta a la partición activa y el equipo comenzará a cargar el sistema operativo almacenado en esa partición activa o un menú de arranque que permita elegir el sistema operativo \(si tiene varios instalados\) a arrancar\.

![](assets%5Cimg%5CUnidad06%5CUnidad06124.png)

* Tamaño de 512 bytes  
* Consta de tres partes
  * Master Boot Code o cargador de arranque   \(446 bytes\)\. Contiene códigos y datos que la BIOS necesita para iniciar la carga del sistema operativo \(SO\)\.
  * Tabla de particiones   \(64 Bytes\)\. Posee información sobre las distribuciones del disco duro\. Información de hasta 4 particiones de 16 bytes cada una\.
  * Firma   \(2 bytes\) → 0x5AA\. Los sistemas operativos utilizan la firma de disco para identificar y diferenciar diferentes dispositivos de almacenamiento de datos y unidades de disco duro en la computadora para el acceso a los datos\.

![](assets%5Cimg%5CUnidad06%5CUnidad06125.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06126.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06127.png)

# 13. GPT (GUID Partition Table)

![](assets%5Cimg%5CUnidad06%5CUnidad06128.png)

GPT \(GUID Partition Table\) es un nuevo estándar para colocar tablas de particiones en medios de almacenamiento\. Forma parte de la \(UEFI\)\.

GPT se localiza al comienzo del disco duro \(  _[Primary GUID](https://es.wikipedia.org/wiki/Tabla_de_particiones_GUID)_  \)\, al igual que el MBR\, pero no en el primero\, sino en el segundo sector\. El primer sector todavía está reservado para MBR \(Protective MBR\) por motivos de seguridad y para conservar la compatibilidad con sistemas más antiguos\.

Los datos críticos para el funcionamiento de la plataforma se almacenan en particiones en lugar de hacerlo en sectores ocultos o no particionados \(como en el caso de MBR\)\.  Además\, los discos GPT incluyen tablas de partición principales redundantes \(Primary GUID\) y de copia de seguridad \(Backup GUID\) a fin de mejorar la integridad de la estructura de datos de la partición\.

![](assets%5Cimg%5CUnidad06%5CUnidad06129.png)

# 13. MBR vs GPT

Con MBR se pueden crear hasta cuatro particiones primarias por disco o bien se pueden crear hasta tres particiones primarias y una partición extendida\. Dentro de la partición extendida se pueden crear un número ilimitado de unidades lógicas\. Los sistemas operativos sólo pueden ir en particiones primarias

Con GPT se pueden crear hasta 128 particiones primarias\.  Desaparece el concepto de particiones extendidas ni unidades lógicas\, todas las particiones son primarias\.

GPT admite volúmenes de un tamaño máximo de 9\.44 ZB\, MBR hasta de 2TB

MBR→ BIOS // GPT→ UEFI

MBR es soportado por sistemas operativos tanto antiguos como modernos mientras que GPT solo es soportado por SO modernos \(a partir de Windows 8\)

![](assets%5Cimg%5CUnidad06%5CUnidad06130.png)

¿Qué pasa si se corrompe MBR?

¿Qué pasa si se corrompe GPT?

![](assets%5Cimg%5CUnidad06%5CUnidad06131.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06132.png)

# 13. Estructura lógica de los discos

<span style="color:#333333"> __Partición primaria\. style="color:#333333"> Puede ser reconocida como una partición de arranque y puede contener un sistema operativo que realice el arranque del equipo\. Una de las particiones primarias se llama la partición activa y es la de arranque\. El ordenador busca en esa partición activa el arranque del sistema\. Cuando hay varios sistemas operativos instalados la partición activa tiene un pequeño programa llamado gestor de arranque que presenta un pequeño menú que permite elegir qué sistema operativo se arranca\. Los sistemas operativos detectarán las particiones primarias y les asignará una unidad\. Límite de 4 en MBR y 128 en GPT\.

![](assets%5Cimg%5CUnidad06%5CUnidad06133.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06134.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06135.png)

<span style="color:#333333"> __Partición extendida\. style="color:#333333"> También conocida como partición secundaria\, sirve para contener múltiples unidades lógicas en su interior\. Fue ideada para romper la limitación de 4 particiones primarias en un solo disco físico por tanto sólo se utiliza en MBR\. Solo puede existir una partición de este tipo por disco\, y solo sirve para contener particiones lógicas\. Por lo tanto\, es el único tipo de partición que  style="color:#333333"> _no_  style="color:#333333"> soporta un sistema de archivos directamente\. No se puede instalar un sistema operativo en ella\.  style="color:#333333"> _Solo aplicable a MBR\._ 

![](assets%5Cimg%5CUnidad06%5CUnidad06136.png)

Disco duro con tres particiones primarias y una extendida\.

<span style="color:#333333"> __Partición lógica\.  style="color:#333333">Ocupa una porción de la partición extendida o la totalidad de la misma\, y se puede formatear con un sistema de archivos diferente \(FAT32\, NTFS\, ext3\, ext4\, etc\.\) y se le asignan una unidad\, así el sistema operativo reconoce las particiones lógicas o su sistema de archivos\.  style="color:#333333"> _Solo aplicable a MBR\._ 

![](assets%5Cimg%5CUnidad06%5CUnidad06137.png)

Disco duro MBR con tres particiones primarias y  una extendida con cuatro lógicas

![](assets%5Cimg%5CUnidad06%5CUnidad06138.png)

Disk Management \- Administrador de discos

![](assets%5Cimg%5CUnidad06%5CUnidad06139.png)

# 14. Sistema de archivos

El sistema de archivos   o File System es un método para el almacenamiento y organización de archivos y los datos que estos contienen\, para hacer más fácil la tarea encontrarlos y acceder a ellos\.

Para ello\, el sistema operativo utiliza las famosas “carpetas” o “directorios” con el fin de organizar todas las rutas y localizar la información contenida en el disco duro\.

La estructura de directorios suele ser jerárquica\, ramificada o en árbol invertido\.

![](assets%5Cimg%5CUnidad06%5CUnidad06140.png)

Los principales tipos sistemas de archivos que encontramos son los siguientes:

NTFS \(New Technology File System\)\.

HPFS \(High Performance File System\)\.

EXT \(Extended file System\)\.

HFS\+ \(Hierarchical File System\)\.

APFS \(Apple File System\)\.

FAT \(File Allocation Table\)\.

exFAT \(Extended File Allocation\)

FAT32\.

ReFS

Para saber cuál de estos tipos debemos elegir debemos saber el sistema operativo que estamos usando o usaremos Windows\, Linux o MacOS\. Esto es importante porque hay algunos sistemas de ficheros que no son compatibles con algunos sistemas operativos:

Windows: NTFS\, FAT32 y exFAT

Linux: EXT4\, NTFS\, exFAT y FAT32

MacOS:   APFS\,   HFS\, HFS EXT4 y NTFS con limitaciones\.

<span  __Actividad sistema de archivos

![](assets%5Cimg%5CUnidad06%5CUnidad06141.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06142.png)

![](assets%5Cimg%5CUnidad06%5CUnidad06143.png)

# 14. Comandos disco duro

Info del disco:   wmic diskdrive get caption\,serialnumber

![](assets%5Cimg%5CUnidad06%5CUnidad06144.png)

Espacio libre:   fsutil volume diskfree c:

![](assets%5Cimg%5CUnidad06%5CUnidad06145.png)

# Bibliografía

_[https://www\.ticarte\.com/contenido/caracteristicas\-fisicas\-de\-los\-discos\-duros\-magneticos](https://www.ticarte.com/contenido/caracteristicas-fisicas-de-los-discos-duros-magneticos)_

_[https://www\.adslzone\.net/reportajes/internet/comparativa\-almacenamiento\-nube/](https://www.adslzone.net/reportajes/internet/comparativa-almacenamiento-nube/)_

_[https://www\.seagate\.com/es/es/tech\-insights/what\-is\-nas\-master\-ti/](https://www.seagate.com/es/es/tech-insights/what-is-nas-master-ti/)_

_[https://pokde\.net/system/pc/storage/sd\-card\-types\-speed\-class\-explained](https://pokde.net/system/pc/storage/sd-card-types-speed-class-explained)_

_[https://www\.xataka\.com/basics/tipos\-tarjetas\-sd\-que\-significan\-sus\-clases\-tipos\-numeraciones](https://www.xataka.com/basics/tipos-tarjetas-sd-que-significan-sus-clases-tipos-numeraciones)_

_[https://www\.xataka\.com/basics/pen\-drive\-memoria\-usb\-que\-sirve](https://www.xataka.com/basics/pen-drive-memoria-usb-que-sirve)_

_[https://es\.wikipedia\.org/wiki/Disco\_compacto](https://es.wikipedia.org/wiki/Disco_compacto)_

_[https://hardzone\.es/reportajes/que\-es/que\-es\-blu\-ray/](https://hardzone.es/reportajes/que-es/que-es-blu-ray/)_

_[https://www\.ticarte\.com/contenido/el\-cd\-rom\-dvd\-y\-blu\-ray\-de\-los\-equipos\-microinformaticos](https://www.ticarte.com/contenido/el-cd-rom-dvd-y-blu-ray-de-los-equipos-microinformaticos)_

_[http://cuartoinformatica\.tecnojulio\.com/2015/10/22/estructura\-logica\-del\-disco\-duro\-actividad\_12/](http://cuartoinformatica.tecnojulio.com/2015/10/22/estructura-logica-del-disco-duro-actividad_12/)_

_[http://www\.carm\.es/edu/pub/04\_2015/2\_5\_2\_contenido\.html](http://www.carm.es/edu/pub/04_2015/2_5_2_contenido.html)_

_[https://informaticoalrescate\.com/2019/08/08/diferencias\-entre\-los\-sistemas\-de\-archivos/](https://informaticoalrescate.com/2019/08/08/diferencias-entre-los-sistemas-de-archivos/)_

_[https://www\.kingston\.com/spain/es/solutions/pc\-performance/difference\-between\-slc\-mlc\-tlc\-3d\-nand\#:~:text=SLC%20ofrece%20el%20mejor%20rendimiento\,utilizarse%20en%20productos%20de%20consumo](https://www.kingston.com/spain/es/solutions/pc-performance/difference-between-slc-mlc-tlc-3d-nand#:~:text=SLC%20ofrece%20el%20mejor%20rendimiento,utilizarse%20en%20productos%20de%20consumo)_  \.

_[https://www\.profesionalreview\.com/2018/03/10/discos\-mbr\-y\-gtp\-diferencias\-entre\-los\-dos\-estandares\-de\-la\-actualidad/](https://www.profesionalreview.com/2018/03/10/discos-mbr-y-gtp-diferencias-entre-los-dos-estandares-de-la-actualidad/)_

_[http://www\.carm\.es/edu/pub/04\_2015/2\_5\_1\_contenido\.htmlb](http://www.carm.es/edu/pub/04_2015/2_5_1_contenido.htmlb)_

_[https://www\.idiskhome\.com/resource/backup/mbr\-vs\-gpt\.shtml](https://www.idiskhome.com/resource/backup/mbr-vs-gpt.shtml)_

[https://www\.profesionalreview\.com/disco\-duro/](https://www.profesionalreview.com/disco-duro/)

[https://www\.diskmfr\.com/know\-how\-internal\-structure\-details\-of\-solid\-state\-drives/](https://www.diskmfr.com/know-how-internal-structure-details-of-solid-state-drives/)

[https://computerhoy\.com/noticias/hardware/que\-es\-ssd\-como\-funciona\-que\-tipos\-existen\-50726](https://computerhoy.com/noticias/hardware/que-es-ssd-como-funciona-que-tipos-existen-50726)

https://gamersnexus\.net/guides/1497\-ssd\-architecture\-1\-what\-is\-tlc\-nand\-mlc\-anatomy

