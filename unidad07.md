![](assets%5Cimg%5CUnidad07%5Cu70.png)

# U7- Adaptadores gráficos, red y multimedia

# MONTAJE Y MANTENIMIENTO DE EQUIPOS

# 1º Ciclo Formativo de Grado Medio de  
Sistemas Microinformáticos y Redes

# Curso 2022/2023

# 1. Tarjetas gráficas

Definición

GPU

Características

Salidas/Conectores de la tarjeta gráfica

Adaptadores

Alimentación

Multi monitor

# Contenidos. Adaptadores de red

Tarjetas de red para LAN

Conectores

Dirección MAC

Velocidad

Wake on LAN (WoL)

Tarjetas de red para Wi-Fi

Estándares WiFi

Bluetooth

# Contenidos. Tarjetas multimedia

Tarjetas de sonido

Funciones de la tarjeta de sonido

Conectores

Componentes de una tarjeta de sonido

Tarjeta capturadora de video

Tarjeta sintonizadora de televisión

# 1.1 Tarjetas gráficas

* La tarjeta gráfica, también llamada  __tarjeta de vídeo,__  adaptador de pantalla o simplemente GPU (heredado del nombre de su procesador gráfico) es una tarjeta de expansión o un circuito integrado que se encarga de procesar los datos que le envía el procesador del ordenador y transformarlos en información visible y comprensible para el usuario, representándolos en el dispositivo de salida, el monitor.
* Tipos:
* __Integradas en __  _CPU_ : Estas gráficas integradas tienen normalmente una potencia reducida y además necesitan recursos de memoria RAM del sistema.
  * Intel
  * Amd → APU
  * Apple M1
* __Tarjetas de expansión:__
  * PCI-Express x16
  * PCI → Obsoleto
  * AGP → Obsoleto

# 1.1 Componentes tarjetas gráficas

![](assets%5Cimg%5CUnidad07%5Cu71.png)

![](assets%5Cimg%5CUnidad07%5Cu72.png)

# 1.2 GPU

__GPU, Graphics Processing Unit o Unidad de Procesamiento de Gráficos__ , se encarga de procesar los gráficos que utiliza el sistema de computación, es decir es una unidad de procesamiento gráfico con una alta capacidad de paralelizado, capaz de trabajar y de procesar gráficos, y de convertir información y datos en elementos visibles por el usuario, pero que también de sacar adelante tareas que requieran de la realización de una gran cantidad de operaciones concurrentes en paralelo

Físicamente es un circuito muy complejo que integra varios miles de millones de transistores y varios núcleos que tienen capacidad de procesamiento independiente.

Así como las CPU, están diseñados con pocos núcleos pero altas frecuencias de reloj, las GPU tienden al concepto opuesto, contando con grandes cantidades de núcleos con frecuencias de reloj relativamente bajas.

![](assets%5Cimg%5CUnidad07%5Cu73.png)

![](assets%5Cimg%5CUnidad07%5Cu74.png)

![](assets%5Cimg%5CUnidad07%5Cu75.png)

# 1.3 Características GPU

* __Núcleos. __  __Cada uno de ellos contribuye al rendimiento en conjunto de la tarjeta gráfica. Cada fabricante utiliza diferentes arquitecturas, y no es un buen dato para comparar modelos de fabricantes distintos.__
  * __AMD→ Stream Processors__
  * __NVIDIA → CUDA Cores__
* __Velocidad o frecuencia base de reloj.__  __ Indica la velocidad a la que operan los núcleos de la tarjeta gráfica. Las frecuencias de las tarjetas gráficas son mucho menores que las de los procesadores.__
  * __Frecuencia de Boost.   __  __Aumento por tiempo limitado de la frecuencia base para acelerar el renderizado de la escena. Lo que se traduce en un aumento de la tasa de fotogramas y/o de la calidad de imagen.__

![](assets%5Cimg%5CUnidad07%5Cu76.png)

__                 __  __     Representación de imágenes__

![](assets%5Cimg%5CUnidad07%5Cu77.png)

__Imagen vectorial__

Objeto definido como un punto central en alguna parte del plano, con un radio de un tamaño concreto, una línea que lo envuelve con un grosor determinado y un color de relleno, rojo en este caso. Las imágenes vectoriales se describen mediante líneas, formas y otros componentes gráficos de imagen almacenados en un formato que incorpora fórmulas geométricas para interpretar los elementos de la imagen.

__Mapa de bits o imagen rasterizada__

Objeto definido como una serie de píxeles de la pantalla pintados en rojo. Consiste en definir el color de cada pixel. Se describen mediante un conjunto o mapa de bits dentro de una cuadrícula rectangular de píxeles o puntos.

![](assets%5Cimg%5CUnidad07%5Cu78.png)

__Imagen rasterizada →__

![](assets%5Cimg%5CUnidad07%5Cu79.png)

__← Imagen vectorial__

Los objetos 3D se guardan en la memoria de forma vectorial, pero para ser representados en un medio 2D, como una pantalla o un papel, se deben convertir a un mapa de bits, a este proceso se le llama rasterización.

La  __rasterización o rasterizar,__  consiste en pasar un objeto vectorial a un conjunto de bits. El proceso contrario sería  __vectorizar.__

__ROPs. (Render/Raster Output Units)__ . Se encargan del proceso de rasterizado. Gestiona la salida de píxeles en la pantalla y así como otras tareas básicas de renderizado y el antialiasing.

![](assets%5Cimg%5CUnidad07%5Cu710.png)

__TMUs o Texture Mapping Unit__  es una unidad fija que se encarga del llamado mapeo de texturas donde lógicamente se encarga de darle las texturas a las formas y píxeles ya trabajados para finalmente rotar o redimensionar estas para hacerlas más reales. Básicamente le da textura a los píxeles procesados.

![](assets%5Cimg%5CUnidad07%5Cu711.png)

![](assets%5Cimg%5CUnidad07%5Cu712.png)

__Pixel Fill Rate o tasa de relleno de píxeles__ . Número de píxeles que una tarjeta de video puede renderizar en pantalla y escribir en la memoria de video, en un segundo.  _Megapíxeles por segundo(MPx/s)_

__Texture Fill Rate o tasa de relleno de texturas. __ número de elementos de mapa de textura (téxeles) que una GPU puede mapear a píxeles en un segundo.  _Megatéxeles(MT/s) o gigatexels por segundo(GT/s)._

La GTX 1080 Ti tiene un Texture Fillrate de 332  __GTexel/s__ , mientras que tiene un Pixel Fillrate de  __130,2 Gpixel/s.__

![](assets%5Cimg%5CUnidad07%5Cu713.png)

![](assets%5Cimg%5CUnidad07%5Cu714.png)

# 1.3 VRAM

* __Video Ram o memoria de vídeo__  __  está integrada en forma de chips sobre el PCB de la tarjeta gráfica, y que cuenta con su propio bus de datos. Es un tipo de memoria diseñada especialmente para llevar a cabo un tipo concreto de tareas en aplicaciones gráficas y videojuegos. __
* __En la memoria VRAM se cargan las texturas y los modelos que la GPU va a utilizar y procesar para crear la imagen después. Por tanto, es muy importante que nuestra tarjeta gráfica posea suficiente memoria VRAM. __
* __Tipo de VRAM:__
  * __GDDR SDRAM__  __ (__  __Graphics Double Data Rate Synchronous Dynamic Random-Access Memory__  __), es el tipo de VRAM de gráficos más popular, y es lo que encontrará en la gran mayoría de las GPUs actuales. → JEDEC__
    * __GDDR5__
    * __GDDR5X__
    * __GDDR6__
    * __GDDR6X__
  * __HBM__  __(High Bandwidth Memory), tipo de memoria gráfica que tiene un ancho de banda mucho mayor que GDDR6, alto coste __
    * __HBM__
    * _[HBM2](https://www.pccomponentes.com/amd-radeon-pro-wx-9100-16gb-gddr5-hbm2)_
    * _[HBM2E](https://hardzone.es/tutoriales/rendimiento/memoria-hbm2e-caracteristicas-especificaciones/)_

__Bus de memoria de la GPU. __  __Realiza la interconexión entre la memoria VRAM de la gráfica la GPU.__

__Ancho de bus de memoria (memory bus width)__  __. Número de bits de datos que pasan por él. El ancho del bus de memoria dictamina cuántos canales distintos tiene el controlador de memorias de la GPU, esto es, la cantidad de chips que puede servir a la vez. En el caso de las memorias GDDR actuales, estaremos hablando de __  _32 bits por chip_  __, por lo que una tarjeta gráfica podrá acceder a la vez a la siguiente cantidad de chips __  __→ __  __Número de chips = Ancho del bus / 32__

__La NVIDIA GT 1030 tiene 64 bits de ancho de bus, la RTX 3080 tiene 320 bits (imagen) y la RTX 3090 tiene 384 bits de ancho de bus.__

![](assets%5Cimg%5CUnidad07%5Cu715.png)

* RTX 3080:
  * 10 chips
  * 32 bits cada chip
* Ancho de bus = 10*32 = 320 bits

__Frecuencia/ velocidad de reloj de la memoria. __  __Operaciones por ciclo de reloj que es capaz de realizar. __  _No confundir con la frecuencia de la GPU_

![](assets%5Cimg%5CUnidad07%5Cu716.png)

__Ancho de banda (BW) de la memoria . __  __El ancho de banda de la memoria es la cantidad de datos a los que la GPU puede acceder en cada ciclo de reloj y depende directamente de la frecuencia de la memoria (MHZ) o velocidad de la memoria(Gbps) y del ancho de bus. Normalmente se mide en GB/s__

__BW__  __memoria__  __= Ancho de bus(bits) * Frecuencia(Mhz) / 8 bytes__

__BW__  __memoria__  __= Ancho de bus(bits) * Velocidad de la memoria(Gbps) / 8 bytes__

__Ejemplo: Una __  _[FX 5900XT](https://technical.city/es/video/GeForce-FX-5900-XT)_  __, cuya velocidad de memoria es de 700MHz y cuyo bus de memoria es de 256bits:__

__BW__  __memoria__  __= __  __700 MHz*256 bits = 179200 bits/s ⇒ __  __179200 bits/s__  __ / 8 bytes = 22400 MB/s = 22,4 GB/s.__

![](assets%5Cimg%5CUnidad07%5Cu717.png)

![](assets%5Cimg%5CUnidad07%5Cu718.png)

__BW__  __memoria__  __= Ancho de bus(bits) * Velocidad de la memoria(Gbps)__

__BW__  __memoria__  __=  384 bits * 14 Gbps / 8 bytes= 672 GB/s__

![](assets%5Cimg%5CUnidad07%5Cu719.png)

![](assets%5Cimg%5CUnidad07%5Cu720.png)

__Capacidad.__  La cantidad de memoria de la tarjeta gráfica viene dada por la capacidad individual de cada uno de sus chips

![](assets%5Cimg%5CUnidad07%5Cu721.png)

![](assets%5Cimg%5CUnidad07%5Cu722.png)

__VRM - Voltage Regulator Modules - Módulo de regulación de voltaje. __ Es un componente electrónico que permite regular, con mayor o menor eficiencia, el voltaje que se suministra en un circuito electrónico y en el caso que nos ocupa a la tarjeta gráfica aunque también está presente en procesadores y placas base

![](assets%5Cimg%5CUnidad07%5Cu723.png)

# 1.6 Alimentación

Cuanto más potente sea una tarjeta gráfica mayor es su consumo eléctrico, y el problema radica en que todas las gráficas que necesitan alimentación adicional consumen más energía de lo que el zócalo PCI-Express es capaz de proporcionar, limitado actualmente en 75 vatios. En otras palabras, cualquier tarjeta gráfica que tenga un consumo mayor de 75W necesitará alimentación adicional, y la manera de proporcionársela es conectándola directamente a la fuente de alimentación mediante los cables PCI-E de 6 y 8 pines.

Cada uno de los conectores de los cables PCIe de la fuente de alimentación es capaz de proporcionar 12,5 vatios adicionales. En otras palabras, un conector PCIe de 6 pines es capaz de entregar hasta 75 vatios, mientras que esto se eleva hasta los 100 vatios en los conectores de 8 pines.

![](assets%5Cimg%5CUnidad07%5Cu724.png)

![](assets%5Cimg%5CUnidad07%5Cu725.jpg)

Una tarjeta gráfica que tenga un consumo eléctrico de 150 vatios, necesitaría los 75 que proporciona la placa base y otros 75 a través de la alimentación adicional de la fuente. En este ejemplo, necesitaríamos 75 vatios adicionales, y con un conector de 6 pines sería suficiente. Si la gráfica tuviera un consumo de 225 vatios, necesitaríamos los 75 de la placa y otros 150 adicionales, que podríamos proporcionarle mediante dos conectores de 6 pines, o incluso uno de 6 y otro de 8 para alcanzar los 250 vatios

![](assets%5Cimg%5CUnidad07%5Cu726.png)

# 1.3 TDP vs TGP vs TBP

__TDP - Thermal Design Power. __  __En tarjetas gráficas el término TDP se refiere al __  __consumo de energía que tiene la GPU de la tarjeta.__

__TGP - Total Graphics Power o  consumo gráfico total__  __. Cantidad máxima de potencia que la fuente de alimentación del sistema debería ser capaz de proveer a la tarjeta gráfica. Es decir se tiene en cuenta el consumo de la GPU, que nos lo daba el TDP,  y se le suma el consumo de todo el sistema de memoria (que es bastante significativo) y el del VRM que alimenta a la gráfica. Se usa en gráficas con chip __  _Nvidia._

__TBP - __  __Total Board Power. __ Concepto equivalente a TGP pero para gráficas con chip  _AMD._

![](assets%5Cimg%5CUnidad07%5Cu727.png)

__TDP - Thermal Design Power. __  __En tarjetas gráficas el término TDP se refiere al __  __consumo de energía que tiene la GPU de la tarjeta.__

__TGP - Total Graphics Power o  consumo gráfico total__  __. Cantidad máxima de potencia que la fuente de alimentación del sistema debería ser capaz de proveer a la tarjeta gráfica. Es decir se tiene en cuenta el consumo de la GPU, que nos lo daba el TDP,  y se le suma el consumo de todo el sistema de memoria (que es bastante significativo) y el del VRM que alimenta a la gráfica. Se usa en gráficas con chip __  _Nvidia._

__TBP - __  __Total Board Power. __ Concepto equivalente a TGP pero para gráficas con chip  _AMD._

![](assets%5Cimg%5CUnidad07%5Cu728.png)

# 1.3 Flops / FPS

![](assets%5Cimg%5CUnidad07%5Cu729.png)

![](assets%5Cimg%5CUnidad07%5Cu730.png)

__FLOPS -Floating (point) Operations Per Second - Operaciones en punto flotante por segundo__  __. Se trata de una tasa de velocidad de las tarjetas gráficas. Se suele medir en Gflops o TFlops__

__FPS - Frames Per Second - Imágenes por segundo__  __. Se utiliza ampliamente en el mundo de los videojuegos, ya que a mayor número de FPS, más fluido correrá el juego. Comparando dos tarjetas gráficas diferentes, en el mismo juego y bajo las mismas condiciones, podemos estimar cuál de las dos da más rendimiento simplemente mirando la cantidad de FPS que ofrecen de media.__

# 1.3 Especificaciones tarjeta

![](assets%5Cimg%5CUnidad07%5Cu731.png)

_[https://www.profesionalreview.com/hardware/mejores-tarjetas-graficas/](https://www.profesionalreview.com/hardware/mejores-tarjetas-graficas/)_

![](assets%5Cimg%5CUnidad07%5Cu732.png)

# 1.3 Resolución y aspect ratio

__Resolución. __ Es el número de píxeles que puede ser mostrado en la pantalla. Viene dada por el producto del ancho por el alto, medidos ambos en píxeles, con lo que se obtiene una relación, llamada  __relación de aspecto(aspect ratio)__ . La máxima resolución que puede mostrar una tarjeta gráfica viene directamente determinada por el puerto a través del que lo hagamos.

Un  __pixel__ , en  plural píxeles (acrónimo del inglés picture element) es la menor unidad homogénea en color que forma parte de una imagen digital, ya sea esta una fotografía, un fotograma de vídeo o un gráfico.

![](assets%5Cimg%5CUnidad07%5Cu733.png)

![](assets%5Cimg%5CUnidad07%5Cu734.png)

![](assets%5Cimg%5CUnidad07%5Cu735.png)

# 1.3 Profundidad de color

* __Profundidad de color. __ La profundidad de color o bits por píxel (bpp)  se refiere a la cantidad de bits para representar el color de un píxel en una imagen.
  * Escala grises → Colores = 2 bits
  * RGB →  Colores = 23*bits

![](assets%5Cimg%5CUnidad07%5Cu736.png)

![](assets%5Cimg%5CUnidad07%5Cu737.png)

![](assets%5Cimg%5CUnidad07%5Cu738.png)

# 1.3 Frecuencia de actualización.

__Frecuencia de actualización (velocidad de refresco). __ Es el número de veces por segundo que se dibuja la imagen en la pantalla en un segundo. Se mide en Hercios.

![](assets%5Cimg%5CUnidad07%5Cu739.png)

_[https://hardzone.es/tutoriales/rendimiento/fps-ojo-humano/](https://hardzone.es/tutoriales/rendimiento/fps-ojo-humano/)_

# 1.3 Espacio de color

* __Un espacio de color__  es un sistema de interpretación del color, es decir, una organización específica de los colores en una imagen o video. Depende del modelo de color en combinación con los dispositivos físicos que permiten las representaciones reproducibles de color, por ejemplo las que se aplican en señales analógicas (televisión a color) o representaciones digitales.
  * __RGB __ es un modelo de color basado en la síntesis aditiva, con el que es posible representar un color mediante la mezcla por adición de los tres colores de luz primarios.
    * [sRGB](https://es.wikipedia.org/wiki/Espacio_de_color_sRGB)
    * [Adobe RGB](https://es.wikipedia.org/wiki/Adobe_RGB)
    * _[ProPhoto RGB](https://es.wikipedia.org/w/index.php?title=Espacio_de_color_ProPhoto_RGB&action=edit&redlink=1)_
  * __CMYK (siglas de Cyan, Magenta, Yellow y Key) es un modelo de color sustractivo que se utiliza en la impresión en colores.__

![](assets%5Cimg%5CUnidad07%5Cu740.png)

![](assets%5Cimg%5CUnidad07%5Cu741.png)

![](assets%5Cimg%5CUnidad07%5Cu742.png)

# 1.4 Salidad tarjetas gráficas

Las tarjetas gráficas disponen de unos conectores de salida que sirven para conectarla con los monitores.

![](assets%5Cimg%5CUnidad07%5Cu743.png)

# 1.4 VGA. Video Graphics Array

Sólo puede llevar información analógica de tipo RGBHV (Red, Green, Blue, frecuencia Horizontal, frecuencia Vertical)

Resolución máxima: 2048 x 1536 píxeles a 85 Hz

Conector DB de 15 pines

![](assets%5Cimg%5CUnidad07%5Cu744.png)

![](assets%5Cimg%5CUnidad07%5Cu745.png)

![](assets%5Cimg%5CUnidad07%5Cu746.png)

![](assets%5Cimg%5CUnidad07%5Cu747.png)

# 1.4 DVI (Digital Visual Interface)

* Su parte izquierda está destinada a llevar las señales digitales de la tarjeta gráfica al monitor, mientras  que en su lado derecho están los pines destinados a transmitir la señal analógica.
* Los tres tipos de conectores DVI que podemos encontrar son DVI-A (analógico), DVI-D (digital) y DVI-I (integrado; analógico y digital). Los conectores DVI-I y DVI-D tienen dos velocidades de datos distintas, conocidas como Single-Link (SL) y Dual-Link(DL)
  * SL →1.65 Gbps de ancho de banda lo que permite llegar a 1920 x 1200 píxeles a 60Hz
  * DL→ 2 Gbps de ancho de banda lo que permite llegar 2560 x 1600 píxeles a  60 Hz

![](assets%5Cimg%5CUnidad07%5Cu748.png)

![](assets%5Cimg%5CUnidad07%5Cu749.png)

![](assets%5Cimg%5CUnidad07%5Cu750.png)

![](assets%5Cimg%5CUnidad07%5Cu751.png)

![](assets%5Cimg%5CUnidad07%5Cu752.png)

# 1.4 HDMI (High-Definition Multimedia Interface)

__HDMI__  responde a las siglas High Definition Multimedia Interface (interfaz multimedia de alta definición) y hace referencia a la norma de conexión que permite transmitir audio y vídeo digital sin comprimir desde un equipo a otro y con un único cable.

![](assets%5Cimg%5CUnidad07%5Cu753.png)

![](assets%5Cimg%5CUnidad07%5Cu754.png)

![](assets%5Cimg%5CUnidad07%5Cu755.png)

![](assets%5Cimg%5CUnidad07%5Cu756.png)

![](assets%5Cimg%5CUnidad07%5Cu757.png)

# 1.4 DisplayPort

__DisplayPort__  es una interfaz digital para todo tipo de dispositivos, la cual ha sido desarrollada por VESA, por lo que estamos ante una interfaz que está libre de cualquier tipo de licencia o canon.

![](assets%5Cimg%5CUnidad07%5Cu758.png)

![](assets%5Cimg%5CUnidad07%5Cu759.png)

![](assets%5Cimg%5CUnidad07%5Cu760.png)

# DisplayPort

![](assets%5Cimg%5CUnidad07%5Cu761.png)

![](assets%5Cimg%5CUnidad07%5Cu762.png)

# 1.4 DisplayPort

![](assets%5Cimg%5CUnidad07%5Cu763.png)

![](assets%5Cimg%5CUnidad07%5Cu764.png)

# 1.5 Adaptadores

![](assets%5Cimg%5CUnidad07%5Cu765.png)

![](assets%5Cimg%5CUnidad07%5Cu766.png)

![](assets%5Cimg%5CUnidad07%5Cu767.png)

![](assets%5Cimg%5CUnidad07%5Cu768.png)

![](assets%5Cimg%5CUnidad07%5Cu769.png)

![](assets%5Cimg%5CUnidad07%5Cu770.png)

![](assets%5Cimg%5CUnidad07%5Cu771.png)

# 1.7 Multi-monitor

Conexión de varios monitores a un ordenador

Duplicación de pantalla

Extensión de escritorio

![](assets%5Cimg%5CUnidad07%5Cu772.png)

![](assets%5Cimg%5CUnidad07%5Cu773.png)

# 

# 2.1- Red de área local

Un sistema en red , o una red, es aquel que está formado por dos o más dispositivos conectados entre sí para compartir información, recursos y servicios.

Si nos centramos en una red de área local o LAN es una red de datos de alta velocidad y bajo nivel de errores que abarca un área geográfica relativamente pequeña. La penetración en el mercado de las redes lan es muy alto, es raro no ver una red lan en una empresa o instituciones y cada vez más podemos encontrar redes lan en los hogares.

__Según el medio de transmisión __ podemos encontrar redes de área local

Cableadas basadas en el estándar Ethernet o IEEE 802.3. → Par trenzado (RJ45) o fibra óptica (SPF), Coaxial (BNC) obsoleto

Inalámbricas basadas en el estándar WiFi o IEEE 802.11 → Aire o vacío (Ondas electromagnéticas)

Combinación de ambas ya que que con los elementos hardware adecuados son compatibles entre sí.

# 2.2- Interfaz de red

Los adaptadores de red, tarjeta de red, interfaz de red o NIC (Network interface card) es la parte hardware que comunica los diferentes nodos (ordenador, dispositivos móviles, televisiones….) de la red con el medio de transmisión que a su vez interconecta con los demás dispositivos que conforman la red. Pueden ser cableados o inalámbricos.

![](assets%5Cimg%5CUnidad07%5Cu774.png)

![](assets%5Cimg%5CUnidad07%5Cu775.png)

![](assets%5Cimg%5CUnidad07%5Cu776.png)

![](assets%5Cimg%5CUnidad07%5Cu777.png)

# 2.3- Interfaces de red cableados

![](assets%5Cimg%5CUnidad07%5Cu778.png)

RJ45→ cable par trenzado

SPF→ fibra óptica

BNC→ cable coaxial

![](assets%5Cimg%5CUnidad07%5Cu779.png)

![](assets%5Cimg%5CUnidad07%5Cu780.png)

# 2.3.1- Interfaces de red RJ45

![](assets%5Cimg%5CUnidad07%5Cu781.png)

![](assets%5Cimg%5CUnidad07%5Cu782.png)

![](assets%5Cimg%5CUnidad07%5Cu783.png)

![](assets%5Cimg%5CUnidad07%5Cu784.png)

# 2.3.2. Interfaces de red fibra óptica

Un transceptor SFP (small form-factor pluggable transceptor ) o Mini_GBIC permiten conectar cables de fibra óptica de diferentes tipos, como son monomodo y multimodo, así como diferentes velocidades.

![](assets%5Cimg%5CUnidad07%5Cu785.png)

![](assets%5Cimg%5CUnidad07%5Cu786.png)

![](assets%5Cimg%5CUnidad07%5Cu787.png)

![](assets%5Cimg%5CUnidad07%5Cu788.png)

# 2.3.3. Interfaces de red coaxial

Obsoleto

Redes topologia anillo

![](assets%5Cimg%5CUnidad07%5Cu789.png)

![](assets%5Cimg%5CUnidad07%5Cu790.png)

![](assets%5Cimg%5CUnidad07%5Cu791.png)

![](assets%5Cimg%5CUnidad07%5Cu792.png)

![](assets%5Cimg%5CUnidad07%5Cu793.png)

# 2.3.4- Velocidad Ethernet

Las redes cableadas están basadas en el protocolo Ethernet según IEEE 802.3

MMF: Fibra multimodo (Multi Mode Fiber)

SMF: Fibra monomodo (Single Mode Fiber)

SR: Corto alcance (Short Range)

LR: Largo alcance (Long Range)

![](assets%5Cimg%5CUnidad07%5Cu794.png)

# 2.4- Tarjetas de red inalámbricas

Las redes Wi-Fi permiten la conectividad de equipos y dispositivos mediante ondas de radio.

Estándar IEEE 802.11 → WiFi

![](assets%5Cimg%5CUnidad07%5Cu795.png)

![](assets%5Cimg%5CUnidad07%5Cu796.png)

![](assets%5Cimg%5CUnidad07%5Cu797.png)

![](assets%5Cimg%5CUnidad07%5Cu798.png)

![](assets%5Cimg%5CUnidad07%5Cu799.png)

![](assets%5Cimg%5CUnidad07%5Cu7100.png)

![](assets%5Cimg%5CUnidad07%5Cu7101.png)

# 2.5- Bluetooth

El Bluetooth es un estándar de conectividad inalámbrica presente en nuestros dispositivos electrónicos

IEEE 802.15.1

Frecuencia 2,402 GHz y los 2,480 GHz

![](assets%5Cimg%5CUnidad07%5Cu7102.png)

![](assets%5Cimg%5CUnidad07%5Cu7103.png)

Actividad: ¿NFC?

# 2.6- Dirección MAC (MAC Address)

La dirección MAC (Media Access Control; control de acceso al medio) es un identificador de 48 bits (6 bloques hexadecimales) que corresponde de forma única a una tarjeta o dispositivo de red, es decir cada tarjeta de red tiene su propia y única dirección MAC

Las direcciones MAC son únicas a nivel mundial, y es asignada por el fabricante de la tarjeta.

Se conoce también como dirección física, un ejemplo de MAC es: 00-0F-EA-3F-64-22

__Actividad: Identifica la MAC de tu ordenador y de tu teléfono móvil__

# 2.7- Dispositivos interconexión. Router/Switch

![](assets%5Cimg%5CUnidad07%5Cu7104.png)

# 2.7- Dispositivos interconexión. AP

![](assets%5Cimg%5CUnidad07%5Cu7105.png)

# 2.7- Dispositivos interconexión. Firewall

![](assets%5Cimg%5CUnidad07%5Cu7106.png)

# 2.8- VoIP - Voice Over IP

VoIP es un acrónimo de Voz sobre Protocolo de Internet (Voice Over Internet Protocol), el cual por sí mismo significa voz a través de internet. Es una tecnología que proporciona la comunicación de voz y sesiones multimedia (tales como vídeo) sobre Protocolo de Internet (IP).

![](assets%5Cimg%5CUnidad07%5Cu7107.png)

# 3- Tarjetas multimedia

3.1 Tarjetas de sonido

3.2 Tarjeta capturadora de video

3.3 Tarjeta sintonizadora de TV

# 3.1- Tarjetas de sonido

Es un dispositivo que permite la reproducción, la grabación y la digitalización del sonido, normalmente a través de un software específico.

Las placas base de los equipos actuales normalmente disponen del sistema de sonido integrado y suelen ser de gran calidad. Es por lo tanto poco usual que se amplíen estos equipos con tarjetas de expansión de sonido, salvo en casos muy específicos, como pueden ser una avería o la necesidad de un sistema profesional de sonido, como los usados por músicos o compositores.

Las operaciones más usuales que ejecuta una tarjeta de sonido son:

Grabación. El sonido que se recoge normalmente a través de un micrófono llega a la tarjeta a través de los conectores. Esta señal se recoge, se procesa y se almacena en el formato seleccionado.

Reproducción. La señal digitalizada de un sonido se envía a la tarjeta que la procesa y la manda a través de los conectores de salida hacia los altavoces, auriculares, etcétera.

Síntesis. Es el procedimiento mediante el cual estas tarjetas reproducen sonidos a partir de datos o representaciones simbólicas.

# 3.1- Tarjetas de sonido Sound Blaster

La familia Sound Blaster de tarjetas de sonido, ha sido durante muchos años el estándar para el audio de los PC, antes de que el audio de PC se hiciera común. El creador de Sound Blaster es una empresa de Singapur llamada Creative Technology, también conocida por el nombre de su empresa satélite en los Estados Unidos, Creative Labs.

![](assets%5Cimg%5CUnidad07%5Cu7108.png)

![](assets%5Cimg%5CUnidad07%5Cu7109.png)

![](assets%5Cimg%5CUnidad07%5Cu7110.jpg)

# 3.1- Componentes de una tarjetas de sonido

# 3.1- In/Out de una tarjeta de sonido

![](assets%5Cimg%5CUnidad07%5Cu7111.png)

Analógicos

__Verde __ : Salida de línea. Altavoces frontales. Auriculares.

__Rosa__ : Micrófono

__Azul claro__ : Entrada de Línea

__Naranja:__  Altavoz Subwoofer y Altavoz Central

__Negro:__  Altavoces de sonido envolvente 5.1 ó 7.1 traseros

Digitales S/PDIF

__Coaxial__

__Óptico__

![](assets%5Cimg%5CUnidad07%5Cu7112.png)

Actividad: explicar conectores

# 3.1- Tarjetas de sonido. Home Cinema 5.1

![](assets%5Cimg%5CUnidad07%5Cu7113.png)

![](assets%5Cimg%5CUnidad07%5Cu7114.png)

![](assets%5Cimg%5CUnidad07%5Cu7115.png)

![](assets%5Cimg%5CUnidad07%5Cu7116.png)

![](assets%5Cimg%5CUnidad07%5Cu7117.png)

# 3.1- Tipos de tarjetas de sonido

__    Integradas en placa base: __

![](assets%5Cimg%5CUnidad07%5Cu7118.png)

__   PCI/PCI Express __

![](assets%5Cimg%5CUnidad07%5Cu7119.png)

![](assets%5Cimg%5CUnidad07%5Cu7120.png)

__USB:__

![](assets%5Cimg%5CUnidad07%5Cu7121.png)

![](assets%5Cimg%5CUnidad07%5Cu7122.png)

__Interfaces de audio:__

Similares a las tarjetas de sonido, pero muy enfocadas al uso profesional y a la producción, las interfaces de audio son herramientas dedicadas al uso profesional que cuentan suelen contar con mejores capacidades que sus homónimas internas. Suelen conectarse a través de USB o Firewire de manera externa a nuestros equipos.

![](assets%5Cimg%5CUnidad07%5Cu7123.png)

![](assets%5Cimg%5CUnidad07%5Cu7124.png)

![](assets%5Cimg%5CUnidad07%5Cu7125.png)

__Mesa de mezclas:__

Dispositivo electrónico al cual se conectan diversos elementos emisores de audio, tales como micrófonos, entradas de línea, samplers, sintetizadores, reproductores de CD, etc. Una vez que las señales sonoras entran en la mesa estas pueden ser procesadas y tratadas de diversos modos para dar como resultado de salida una mezcla de audio, mono, multicanal o estéreo

![](assets%5Cimg%5CUnidad07%5Cu7126.png)

# 3.1- Conectores de audio

![](assets%5Cimg%5CUnidad07%5Cu7127.png)

# 3.2- Capturadora de video

Las capturadoras de vídeo son un dispositivo que recibe información de una fuente ajena a nuestro PC o portátil y la codifica como señal digital antes de que se retransmita  o grabe en este último. Técnicamente se consideran un periférico de entrada y pueden recibir señales tanto analógicas como digitales según el modelo de capturadora.

Internas y externas

![](assets%5Cimg%5CUnidad07%5Cu7128.png)

![](assets%5Cimg%5CUnidad07%5Cu7129.png)

![](assets%5Cimg%5CUnidad07%5Cu7130.png)

Una capturadora de vídeo cuenta con dos partes esenciales: una conexión desde el dispositivo a grabar (analógico o digital) a la capturadora y otra desde la propia capturadora dirigida al PC. El tipo de cable empleado suele variar dependiendo de los periféricos, dado que aquellos que consideramos “analógicos” a menudo no cuentan con puertos USB o HDMI, empleando en su lugar variantes como el RCA. En ese momento nuestro ordenador decodifica la señal y, o bien se graba o bien se envía a través de la plataforma de streaming que estemos utilizando. En general podemos distinguir cuatro funciones:

__Capturar__ : se extrae tanto audio como vídeo en S-Video, o compuesto o RGB, bien con cable analógico o vídeo digital HDMI o  HD-SDI.

__Grabar__ : guardamos nuestra actividad en formato digital compatible con cualquier ordenador.

__Transmitir/streaming:__  compartimos nuestra actividad en directo con una audiencia gracias a una plataforma específica.

__Codificar:__  toma nuestra grabación y la convierte a un formato diferente, como el códec de vídeo de alta compresión H.264.

![](assets%5Cimg%5CUnidad07%5Cu7131.png)

A la hora de escoger una capturadora de vídeo tenemos que tener en cuenta el dispositivo de origen (consola, PC, Playstation 4, Xbox One, Xbox series X Playstation 5, Nintendo Switch, etc…) para así adquirir un modelo compatible.

También tenemos que vigilar el número de complementos (cables, conectores, adaptadores) incluidos inicialmente con la capturadora o que debamos adquirir a parte

![](assets%5Cimg%5CUnidad07%5Cu7132.jpg)

_[https://obsproject.com/es](https://obsproject.com/es)_

![](assets%5Cimg%5CUnidad07%5Cu7133.png)

# 3.2- Capturar pantalla

![](assets%5Cimg%5CUnidad07%5Cu7134.png)

![](assets%5Cimg%5CUnidad07%5Cu7135.png)

![](assets%5Cimg%5CUnidad07%5Cu7136.png)

_[https://getgreenshot.org/](https://getgreenshot.org/)_

# 3.3- Sintonizadora TV

Son dispositivos que permiten sintonizar diferentes canales de televisión en la pantalla del ordenador a través de la señal que proviene de una antena externa o portátil.

Externas o internas

Digitales. Sintonizan los canales digitales de la Televisión Digital Terrestre (TDT).

Satélite. Sintonizan los canales recibidos por antena parabólica.

Híbridas. Sintonizan dos o más tipos de señal.

![](assets%5Cimg%5CUnidad07%5Cu7137.png)

![](assets%5Cimg%5CUnidad07%5Cu7138.png)

![](assets%5Cimg%5CUnidad07%5Cu7139.png)

# 3.4- Otras tarjetas de expansión

Además de estas tarjetas más habituales, en el mercado hay otros tipos de tarjetas de expansión, entre las que se encuentran las de ampliación de puertos, las adaptadoras y controladoras de disco, etc.

![](assets%5Cimg%5CUnidad07%5Cu7140.png)

![](assets%5Cimg%5CUnidad07%5Cu7141.png)

__Tarjetas controladoras de disco: __  La tarjeta controladora de discos se utiliza para añadir más puertos de una determinado interfaz a nuestra placa base, ya sea más puertos a una ya existente o nuevos puertos a una interfaz que no poseía nuestra placa base. Aunque se denomine comúnmente "controladora de discos", en estos puertos se puede conectar cualquier dispositivo de almacenamiento, no solamente discos duros. Además, algunas de estas controladoras de discos, poseen tecnología RAID que podremos aplicar a los discos duros que conectemos a ella.

![](assets%5Cimg%5CUnidad07%5Cu7142.png)

![](assets%5Cimg%5CUnidad07%5Cu7143.png)

__Tarjetas de ampliación de puertos: __  En el caso de que en un equipo informático sean necesarios más puertos de algún tipo específico, una de las soluciones más utilizadas es la instalación de una tarjeta de ampliación de puertos (USB, Firewire, Thunderbolt)

![](assets%5Cimg%5CUnidad07%5Cu7144.png)

![](assets%5Cimg%5CUnidad07%5Cu7145.png)

![](assets%5Cimg%5CUnidad07%5Cu7146.png)

__Tarjetas adaptadoras: __  Se utilizan cuando se dispone de un periférico o dispositivo diseñado para un sistema hardware específico y se quiere instalar en un ordenador que no dispone de ese tipo de bus, socket, conector, etc.

PCI a PCI Express

PCI Express a PCI

PCI Express a NVMe

![](assets%5Cimg%5CUnidad07%5Cu7147.png)

![](assets%5Cimg%5CUnidad07%5Cu7148.png)

# Bibliografía

Libro Montaje y Mantenimiento de Equipos Editorial: McGraw Hill

_[https://hardzone.es/reportajes/que-es/gpu-caracteristicas-especificaciones/](https://hardzone.es/reportajes/que-es/gpu-caracteristicas-especificaciones/)_

_[https://www.xataka.com/basics/tarjeta-grafica-que-que-hay-dentro-como-funciona](https://www.xataka.com/basics/tarjeta-grafica-que-que-hay-dentro-como-funciona)_ .

_[https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/](https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/)_

_[https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/](https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/)_

_[https://hardzone.es/2018/08/26/vga-dvi-hdmi-displayport-salidas-video/](https://hardzone.es/2018/08/26/vga-dvi-hdmi-displayport-salidas-video/)_

_[https://hardzone.es/reportajes/comparativas/diferencias-conectores-dvi/](https://hardzone.es/reportajes/comparativas/diferencias-conectores-dvi/)_

_[https://es.wikipedia.org/wiki/Modelo_de_color_CMYK](https://es.wikipedia.org/wiki/Modelo_de_color_CMYK)_

_[https://es.wikipedia.org/wiki/RGB](https://es.wikipedia.org/wiki/RGB)_

_[https://www.hardware-corner.net/guides/guide-to-computer-ports-and-connectors/](https://www.hardware-corner.net/guides/guide-to-computer-ports-and-connectors/)_

_[https://www.adslzone.net/reportajes/tecnologia/bluetooth/](https://www.adslzone.net/reportajes/tecnologia/bluetooth/)_

_[https://www.datacentermarket.es/tendencias-tic/voz-experto/1120929032809/cableado-proxima-oleada-de-redes-inalambricas-empresas.1.html](https://www.datacentermarket.es/tendencias-tic/voz-experto/1120929032809/cableado-proxima-oleada-de-redes-inalambricas-empresas.1.html)_

_[https://es.wikipedia.org/wiki/Sound_Blaster#Primeras_Sound_Blasters:_El_primer_pack](https://es.wikipedia.org/wiki/Sound_Blaster#Primeras_Sound_Blasters:_El_primer_pack)_

_[https://helpx.adobe.com/es/photoshop-elements/key-concepts/raster-vector.html](https://helpx.adobe.com/es/photoshop-elements/key-concepts/raster-vector.html)_

_[https://www.profesionalreview.com/2021/02/07/tgp-vs-tdp-vs-tbp/](https://www.profesionalreview.com/2021/02/07/tgp-vs-tdp-vs-tbp/)_

_[https://www.estudiomarhea.net/manual-de-sonido-08-la-mesa-de-mezclas/](https://www.estudiomarhea.net/manual-de-sonido-08-la-mesa-de-mezclas/)_

_[https://hardzone.es/tutoriales/componentes/tipo-conexiones-audio/](https://hardzone.es/tutoriales/componentes/tipo-conexiones-audio/)_

