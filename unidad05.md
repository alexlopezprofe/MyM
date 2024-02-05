# T5. Memoria RAM

# 1. Definición de memoria RAM

<span style="color:#000000">La RAM o memoria de acceso aleatorio \(en inglés: Random Access Memory\)\, es la memoria principal de un equipo microinformático y se encarga de almacenar de manera </span>  <span style="color:#000000"> _temporal_ </span>  <span style="color:#000000"> tanto las instrucciones como los datos que ejecuta el microprocesador\.</span>

<span style="color:#000000">Es una memoria volátil\, es decir\, la información se pierde al interrumpirse el flujo eléctrico \(apagar el ordenador\)\.</span>

<span style="color:#000000">Se denominan «de acceso aleatorio» porque se puede leer o escribir en una posición de memoria con un tiempo de espera igual para cualquier posición\.</span>

<span style="color:#000000">Físicamente es un conjunto de chips soldados sobre una PCB\, a este conjunto de chips\, se le denomina </span>  <span style="color:#000000"> _módulo_ </span>  <span style="color:#000000"> de memoria RAM\.</span>

<span style="color:#000000">Los fabricantes tienen que fabricar los módulos de memoria siguiendo los estándares marcados por </span>  _[JEDEC](https://www.jedec.org/)_  <span style="color:#000000">\( Joint Electron Device Engineering Council\)</span>

![](assets/img/Unidad05/Unidad51.png)

![](assets/img/Unidad05/Unidad52.png)

# 1. Estructura módulo memoria RAM

![](assets/img/Unidad05/Unidad53.png)

![](assets/img/Unidad05/Unidad54.png)

![](assets/img/Unidad05/Unidad55.png)

![](assets/img/Unidad05/Unidad56.png)

# 1. SPD. Serial Presence Detect chip

![](assets/img/Unidad05/Unidad57.png)

![](assets/img/Unidad05/Unidad58.png)

<span style="color:#000000"> __Circuito SPD__ </span>  <span style="color:#000000"> \(Serial Presence Detect chip\): Es el encargado de almacenar datos relativos al módulo de memoria RAM\, como el tamaño de la memoria\, el tiempo de acceso\, la velocidad y el tipo de memoria\. De esta forma el ordenador conocerá que memoria RAM tiene instalada de manera automática sin intervención del usuario\.</span>

# 1. PMIC - Power management integrated circuits

PMIC\, Power management integrated circuits o Circuitos integrados de gestión de energía

Exclusivo de DDR5

Chip situado en el centro de las memorias DDR5 y se encarga de gestionar la energía \(voltajes\) del módulo

Permite\, entre otras cosas\, la implementación de una tecnología de sincronización multifásica\. Una novedad que permite realizar transmisiones a un voltaje más bajo o más alto si es necesario\. Ahora será siempre gestionado desde el propio módulo de memoria DDR5\.

![](assets/img/Unidad05/Unidad59.png)

![](assets/img/Unidad05/Unidad510.png)

# 1. Making Memory Chips – Process Steps

![](assets/img/Unidad05/Unidad511.jpg)

_[https://www\.crucial\.es/articles/about\-memory/how\-is\-memory\-made](https://www.crucial.es/articles/about-memory/how-is-memory-made)_

# 2. Estructura interna

<span style="color:#000000"> __Bank \(Bancos de memoria\)\.__ </span>  <span style="color:#000000"> Son los componentes físicos encargados de almacenar los registros de memoria\. Lo forman chips de circuitos integrados\(IC\) que están compuestos en su interior por transistores y capacitores que forman celdas de almacenamiento lo que permite almacenar bits de información dentro de ellos\. </span>  <span style="color:#000000"> __Un chip contiene varios bancos\, __ </span>  <span style="color:#000000">cada banco está distribuido en filas y columnas y la intersección de estas son los bits\.</span>

<span style="color:#000000"> __Rank \(Rango de memoria\)\. __ </span>  <span style="color:#000000">El término rango \(Rank\) fue creado y definido por el JEDEC y es un conjunto de chips conectados entre sí que son accedidos por el controlador de memoria al mismo tiempo formando un bloque o área de datos\. El tamaño de un rango es de 64 bits \(si tiene ECC se añaden 8 bits más\)</span>

![](assets/img/Unidad05/Unidad512.png)

![](assets/img/Unidad05/Unidad513.png)

![](assets/img/Unidad05/Unidad514.png)

![](assets/img/Unidad05/Unidad515.png)

# 2. Rank

![](assets/img/Unidad05/Unidad516.png)

<span style="color:#000000">No todas las memorias tienen el mismo número de chips ni la misma capacidad\, es decir\, su </span>  <span style="color:#000000"> __wide o ancho de bus __ </span>  <span style="color:#000000">no es el mismo\. En las memorias DDR4 actuales podemos encontrar chips con un ancho de bus individual de 4\, 8 o 16 bits \(nomenclaturas de X4\, X8 o X16\)\.</span>

<span style="color:#000000">La interfaz de comunicación de la RAM con la CPU es de 64 bits → </span>  <span style="color:#000000"> _Cada Rank es un conjunto de chips que forman 64 bits_ </span>  <span style="color:#000000"> \(4 chips de 16 bits\, 8 chips de 8 bits o 16 chips de 4 bits\)</span>

<span style="color:#000000"> __ Single vs Dual vs Quad Rank__ </span>

<span style="color:#2C2F34"> __Single Rank__ </span>  <span style="color:#2C2F34">: Memoria RAM con un solo bus de datos de 64 bits será determinada como Single Rank o 1R\. Un módulo Single Rank tendrá una nomenclatura similar a alguna de estas → 1Rx4\, 1Rx8 o 1Rx16\. </span>

<span style="color:#2C2F34"> __Dual Rank__ </span>  <span style="color:#2C2F34">: Si un módulo tiene 2 buses de datos de 64 bits\. \(2R\) →  2Rx4\, 2Rx8 o 2Rx16</span>

<span style="color:#2C2F34"> __Quad Rank:__ </span>  <span style="color:#2C2F34"> </span>  <span style="color:#2C2F34">Si un módulo tiene 4 buses de datos de 64 bits</span>  <span style="color:#2C2F34">\. \(4R\) → 4Rx8 o 4Rx16</span>

<span style="color:#2C2F34"> _No da pistas claras de la capacidad del módulo de memoria_ </span>  <span style="color:#2C2F34">\, ya que los chips pueden ser de 512 MB\, 1 GB\, 2 GB o incluso más\. Claro que sabiendo los rangos que tiene y la capacidad\, podremos adivinar el bus y capacidad individual de ellos\.</span>

![](assets/img/Unidad05/Unidad517.png)

![](assets/img/Unidad05/Unidad518.png)

# 2. Estructura interna

![](assets/img/Unidad05/Unidad519.png)

# 2. Comunicación memoria-procesador → IMC

<span style="color:#000000">IMC → Circuito digital que controla el flujo de datos que va y viene entre el propio procesador y la memoria RAM</span>

<span style="color:#000000">Los controladores de memoria contienen la lógica necesaria para leer y escribir en la memoria RAM</span>

<span style="color:#000000">Podemos encontrar IMCs que disponen de dos controladores de memoria funcionando en paralelo\. Son posicionados en dos “buses” separados llamados también </span>  <span style="color:#000000"> _canales_ </span>  <span style="color:#000000">\. Esto permite que haya varias operaciones de lectura y escritura a la vez\. La ventaja de esto es que en teoría la totalidad del ancho de banda se duplica\. </span>

![](assets/img/Unidad05/Unidad520.png)

![](assets/img/Unidad05/Unidad521.png)

# 2. Single Channel vs Dual Channel

<span style="color:#000000">Single Channel describe cualquier configuración en la que su CPU solo tiene acceso a un solo bus de 64 bits de ancho \(en DDR4\) para acceder a la memoria\.</span>

<span style="color:#000000">La tecnología Dual\-Channel o Doble canal es una tecnología que aumenta el rendimiento porque se permite el paso simultáneo a los 2 módulos de memoria RAM duplicando \(teóricamente\*\) el ancho de banda entre la memoria y la CPU pero en n la práctica no pasa de un 20 a 45%\.</span>

<span style="color:#000000">Para disponer de Dual\-Channel\, la placa base lo debe soportar\. Además hay que instalar 2 módulos de memoria idénticos: mismos timings\, capacidad\, etc\.</span>

![](assets/img/Unidad05/Unidad522.png)

![](assets/img/Unidad05/Unidad523.png)

![](assets/img/Unidad05/Unidad524.png)

![](assets/img/Unidad05/Unidad525.png)

![](assets/img/Unidad05/Unidad526.png)

# 3.1. Capacidad

<span style="color:#000000">Capacidad hace referencia a la cantidad de datos que se pueden almacenar en la RAM\. La memoria RAM es un almacén de datos y lógicamente una característica importante es cuántos datos puede almacenar\. </span>

<span style="color:#000000">Los transistores del interior de los bancos de memoria tienen un determinado tamaño\, con lo cual a menor tamaño de transistor mayor densidad de celdas lo que implica más capacidad\.</span>

<span style="color:#000000">Esta capacidad se mide actualmente en los módulos DDR en GB \(GigaBytes\)\.</span>

<span style="color:#000000">La cantidad de memoria estará directamente relacionada con el uso que hagas del equipo\. Cada uso requiere una cantidad de RAM diferente\. No se necesita la misma memoria RAM para navegar\, que para jugar o editar vídeo o fotos\.</span>

![](assets/img/Unidad05/Unidad527.png)

# 3.2. Velocidad o frecuencia de reloj

* <span style="color:#000000">Los chips de memoria integrados en cada módulo de memoria funcionan a una frecuencia de trabajo determinada\.</span>
* <span style="color:#000000">Este valor se mide en MHz\, por lo tanto\, a mayor cantidad de Megahercios\, mayor velocidad tendrá el módulo\.</span>
  * <span style="color:#000000">En las memorias de tipo DDR \(DOUBLE data rate\) se realizan 2 operaciones por cada ciclo de reloj  y no una como en las SDR\, por tanto  los 3200 MHz anunciados serían en realidad 3200 MT/s \(millones de transferencias por segundo\) y la frecuencia real sería la mitad\, es decir 1600MHz\.</span>
  * <span style="color:#000000">Por ejemplo\, 3200 MHz significa que se tardan 1/3200MHz = 0\,3125 nanosegundos por cada ciclo de reloj\.</span>
  * <span style="color:#000000">Al elegir la memoria RAM\, hay que asegurarse de que la placa base soporta la frecuencia de trabajo de la memoria RAM\.</span>
* <span style="color:#000000">Al instalar algunos módulos de memoria\, la placa puede configurarlos para que trabajen a una frecuencia inferior a la que el fabricante prometía\. En ese caso se tendrá que configurar la frecuencia de la memoria RAM manualmente desde la BIOS o UEFI para subir el multiplicador de sus frecuencias y hacer que funcionen a la velocidad correcta\.</span>

![](assets/img/Unidad05/Unidad528.png)

<span style="color:#000000">Crucial DDR4 </span>  _2400_  <span style="color:#000000"> PC4\-</span>  <span style="color:#00FF00">19200 </span>  <span style="color:#000000">4GB →</span>

<span style="color:#000000"> __La tasa de transferencia de datos__ </span>  <span style="color:#000000"> se refiere a cuántos bits puede transferir un módulo en un tiempo concreto\.</span>

<span style="color:#000000">Tasa de transferencia de datos=</span>  _2400Hz_  <span style="color:#000000">\*8B=</span>  <span style="color:#00FF00">19200</span>  <span style="color:#000000">MB/s</span>

# 3.2. SDR vs DDR

![](assets/img/Unidad05/Unidad529.png)

# 3.2. Ancho de banda

<span style="color:#000000">El ancho de banda máximo de memoria es la velocidad máxima a la cual el procesador puede leer o almacenar datos en una memoria\(en GB/s\)\.</span>

<span style="color:#000000">El ancho de banda máximo teórico de la memoria se puede calcular multiplicando la frecuencia de la memoria multiplicado por el número de bytes de ancho y multiplicado por el número de canales \(o interfaces\) compatibles con el  procesador\.</span>

<span style="color:#000000">La frecuencia de reloj DRAM de la RAM \-> Dato de fabricante/2</span>

<span style="color:#000000">Ancho Bus de la memoria \-> actualmente y desde hace años es de </span>  <span style="color:#000000"> _64 bits por canal \(32\*2 en DDR5\)_ </span>  <span style="color:#000000">\,</span>

<span style="color:#000000">Número ciclo de reloj \-> SDR=1 \(1 operación por ciclo\) y </span>  <span style="color:#000000"> _DDR_ </span>  <span style="color:#000000">=2 \(2 operaciones por ciclo \)</span>

<span style="color:#000000">Número de canales \(Interfaces\) \-> o lo que es igual\, el número de canales máximos de memoria que pueden funcionar al mismo tiempo\. Esto lo determina la plataforma en sí misma\, donde actualmente en escritorio tenemos\(Single\-Channel = 1\) \(Dual\-Channel = 2\) o \(Quad\-Channel= 4 \) disponibles\.</span>

<span style="color:#000000"> __BW = FrecuenciaReal\*64\*Número de ciclos de reloj\*Canales __ </span>

<span style="color:#000000"> _Team Group Delta White RGB DDR4 _ </span>  <span style="color:#000000"> _3200_ </span>  <span style="color:#000000"> _ PC4\-25600_ </span>  <span style="color:#000000"> __ → Frecuencia=3200Mhz/2=1600Mhz__ </span>

__BW\(Dual\-Channel\)=160000000\*64\*2\*__  _2_  __ = 409\.600\.000\.000 bits por segundo = 51\,2 GB/s __

__BW\(Quad\-Channel\)=160000000\*64\*2\*__  _4_

<span style="color:#000000"> __BW = FrecuenciaReal\*64\*Número de ciclos de reloj\*Canales __ </span>

# 3.3. Latencia

<span style="color:#000000">La estructura interna de la memoria RAM es como la de un tablero de ajedrez tridimensional en el que cada cuadro del tablero es una celda en la que se escriben los datos que se almacenan\.</span>

<span style="color:#000000">La latencia es el tiempo que tarda la memoria RAM en situarse en una determinada celda para leer o escribir su contenido\. Cuanto mayor sea la latencia de la memoria RAM\, mayor es el tiempo que “pierde” en llegar a una determinada celda y\, por lo tanto\, menos eficiente en su trabajo\.</span>

<span style="color:#000000">Por lo tanto\, a igualdad de frecuencias de reloj para un módulo de memoria RAM\, es preferible elegir una memoria RAM con una latencia baja\.</span>

![](assets/img/Unidad05/Unidad530.png)

_[https://pcpro\.es/guias/latencia\-memoria\-ram\-que\-es\-y\-tipos/](https://pcpro.es/guias/latencia-memoria-ram-que-es-y-tipos/)_

![](assets/img/Unidad05/Unidad531.png)

![](assets/img/Unidad05/Unidad532.png)

* <span style="color:#000000"> __Timings\.  __ </span>  <span style="color:#000000">Suelen visualizarse en formato numérico: 9\-9\-9\-24 es un ejemplo de tiempos o timings de una memoria DDR\.</span>
* <span style="color:#000000"> __¿Qué significa cada uno de los cuatro números?__ </span>
* <span style="color:#58585A"> __Latencia CAS \(Column Address Strobe\) \(CL\):__ </span>  <span style="color:#58585A"> </span>  <span style="color:#000000">Ciclos de reloj que pasan desde que se realiza una petición para leer o escribir un dato hasta que dicha información está disponible\, o los ciclos de reloj que transcurre entre que el controlador de memoria envía una petición para leer una posición de memoria y el momento en que los datos son enviados a los pines de salida del módulo\.  </span>  <span style="color:#000000"> _Es el dato más importante de esta lista de números\._ </span>
  * <span style="color:#000000">Los tipos de memoria nueva suelen tener una latencia CAS mucho más alta que sus modelos comparables más antiguos\.</span>
* _[https://www\.crucial\.es/articles/about\-memory/difference\-between\-speed\-and\-latency](https://www.crucial.es/articles/about-memory/difference-between-speed-and-latency)_  <span style="color:#000000"> </span>
* <span style="color:#58585A"> __Retardo de columna y fila \(tRCD o Time RAS to CAS Delay\)__ </span>  <span style="color:#58585A">: Número mínimo de ciclos de reloj necesarios para abrir una fila y acceder a una columna\. Se puede considerar el tiempo mínimo que tarda la RAM en llegar a la nueva dirección\. El tiempo para leer el primer bit de memoria de una DRAM sin ninguna fila activa seria tRCD \+ CL</span>
* <span style="color:#58585A"> __Tiempo de precarga de fila \(tRP o Time RAS Precharge\):__ </span>  <span style="color:#58585A"> Tiempo que tarda la memoria en tener lista una fila nueva para usar datos\. Significa básicamente el tiempo que tarda en hacer un salto de línea es decir estoy leyendo la fila "5" y paso a la fila "6" el TRP mide el tiempo que tardó en hacer ese cambio de fila "5" a fila "6"\.</span>
* <span style="color:#58585A"> __Tiempo activo de fila \(tRAS\):__ </span>  <span style="color:#58585A"> Número mínimo de ciclos para los que debe estar activa una fila para garantizar que tengamos tiempo suficiente para acceder a la información que contiene\.</span>

![](assets/img/Unidad05/Unidad533.png)

_[Corsair Value Select DDR4 2666Mhz PC4\-21300 8GB CL18](https://www.memoryc.com/24306-8gb-corsair-valueselect-ddr4-2666mhz-cl18-memory-module.html)_

| Memoria | Velocidad de reloj(MT/s) | Frecuencia real(MHz) | Ciclo de reloj (ns) | Latencia CAS | Latencia real (ns) |
| :-: | :-: | :-: | :-: | :-: | :-: |
| DD4 | 2666 | 1333 | 0.75 | 18 | 13.5 |

<span style="color:#58585A">Latencia real </span>  <span style="color:#58585A">\(ns\)</span>  <span style="color:#58585A"> = tiempo de ciclo de reloj </span>  <span style="color:#58585A">\(ns\)</span>  <span style="color:#58585A"> x números de ciclos de reloj\(CAS\)</span>

<span style="color:#000000">Frecuencia real: 2666\(MT/s\) /2 =</span>  <span style="color:#FF00FF">1333MHz</span>

<span style="color:#000000">Ciclo de reloj=1/1333x10</span>  <span style="color:#000000">6</span>  <span style="color:#000000">Hz</span>  <span style="color:#000000"> </span>  <span style="color:#000000">= 0\.75x10</span>  <span style="color:#000000">\-9</span>  <span style="color:#000000">s=</span>  <span style="color:#FF0000">0\.75ns</span>

<span style="color:#000000">Latencia real= 0\.75nsx18=</span>  <span style="color:#0000FF">13\.5ns</span>

![](assets/img/Unidad05/Unidad534.png)

# 3.4. Voltaje

<span style="color:#000000">El voltaje es el valor de tensión a la que el módulo de memoria RAM trabaja\.</span>

<span style="color:#000000">Disminuye a la vez que la tecnología avanza\, es decir el consumo de los módulos DDR5 es inferior al de los módulos DDR4\.</span>

![](assets/img/Unidad05/Unidad535.png)

![](assets/img/Unidad05/Unidad536.png)

# 4. Tipos de memoria RAM

* __Static RAM \(SRAM\)\.__
  * __Comenzó a utilizarse en 1990 y a día de hoy sigue presente en cámaras digitales\, routers o impresoras\.__
  * __Las ventajas de este tipo de memoria es que consume muy poca energía y tiene unos tiempos de acceso muy bajos\. Las desventajas incluyen que tienen unas capacidades muy bajas\, y unos costes de fabricación bastante elevados\.__
  * __Capaz de mantener los datos\, mientras siga alimentada\, sin necesidad de circuito de refresco\.__
* <span style="color:#333333"> __Dynamic RAM \(DRAM\)__ </span>
  * <span style="color:#333333">Puede aceptar una orden de lectura antes de haber terminado de procesar una de escritura \(pipelining\) lo que posibilita la ejecución de varias instrucciones simultáneamente\.</span>
  * <span style="color:#333333">Basada en condensadores\, los cuales pierden su carga progresivamente\, necesitando de un circuito dinámico de refresco cada cierto período</span>
* <span style="color:#333333"> __Synchronous Dynamic RAM \(SDRAM\)__ </span>
  * <span style="color:#333333">Variante mejorada de la memoria SDRAM que mejora la manera en la que procesa la información de lectura y escritura\. «Single Data Rate» significa que se ejecuta una instrucción de lectura y otra de escritura por cada ciclo de reloj del procesador\.</span>
* <span style="color:#333333"> __Single Data Rate Synchronous Dynamic RAM \(SDR SDRAM\)__ </span>
  * <span style="color:#333333">Segunda generación de memoria SDRAM\.</span>
* <span style="color:#333333"> __Double Data Rate Synchronous Dynamic RAM \(DDR SDRAM\)__ </span>
  * <span style="color:#333333">Se estandarizó a partir del año 2000\.</span>
  * <span style="color:#333333">Opera de la misma manera que la SDR SDRAM solo que el doble de rápido\, es decir\, es capaz de realizar dos instrucciones de lectura y dos de escritura por cada ciclo de reloj del procesador\.</span>

# 4. Tipos de DDR SDRAM

<span style="color:#000000"> __Memoria RAM DDR:__ </span>

<span style="color:#000000"> __Memoria RAM DDR2:__ </span>

<span style="color:#000000"> __Memoria RAM DDR3__ </span>  <span style="color:#000000">:</span>

<span style="color:#000000"> __Memoria RAM DDR4:__ </span>

<span style="color:#000000"> __Memoria RAM DDR5:__ </span>

# 5. Formato

<span style="color:#000000"> __DIMM: __ </span>  <span style="color:#333333">El término </span>  <span style="color:#333333"> __DIMM__ </span>  <span style="color:#333333"> es el acrónimo de la expresión “Dual In\-line Memory Module”</span>

<span style="color:#000000"> __SO\-DIMM:__ </span>  <span style="color:#000000"> SO\-DIMM se llama así por las siglas en inglés de “Small Outline Dual In\-line Memory Module”\, y es precisamente esas palabras «Small Outline» lo que las diferencia de los módulos DIMM habituales\. La diferencia es meramente física\, ocupan un menor espacio y así se pueden instalar en equipos de tamaño reducido como los portátiles\.</span>

![](assets/img/Unidad05/Unidad537.png)

# 5.1 Tipos de DDR SDRAM en formato DIMM

![](assets/img/Unidad05/Unidad538.png)

<span style="color:#000000"> __Longitud: __ </span>  <span style="color:#000000">133\,35 mm</span>

<span style="color:#000000"> __Pines:__ </span>

<span style="color:#000000">DDR:  184 pines</span>

<span style="color:#000000">DDR2: 240 pines </span>

<span style="color:#000000">DDR3: 240 pines </span>

<span style="color:#000000">DDR4: 288 pines</span>

<span style="color:#000000">DDR5: 288 pines </span>

![](assets/img/Unidad05/Unidad539.png)

![](assets/img/Unidad05/Unidad540.png)

| Tipo | Pines | Longitud |
| :-: | :-: | :-: |
| SO-DIMM DDR | 200 | 67.6 mm |
| SO-DIMM DDR2 | 200 | 67.6 mm |
| SO-DIMM DDR3 | 204 | 67.6 mm |
| SO-DIMM DDR4 | 260 | 69.6 mm |
| SO-DIMM DDR5 | 262 |  |

![](assets/img/Unidad05/Unidad541.png)

_[Detalle de la muesca](https://upload.wikimedia.org/wikipedia/commons/9/95/Laptop_SODIMM_DDR_Memory_Comparison_V2.svg)_

# 7. RAM ECC

<span style="color:#58585A">En la memoria principal\, los contenidos son almacenados en forma de código binario\, en otras palabras\, están compuestos por unos y ceros para que el ordenador pueda procesarlos\. Los dígitos binarios se conocen como bits\. Factores como \(fluctuaciones del voltaje\, overclocking\, módulos de memoria defectuosos y viejos\, o radiación de alta energía\) pueden generar un error de bit\. Estos fallos de bit se presentan cuando un bit toma el valor falso\, es decir “1” en vez de “0” y viceversa\. En muchas aplicaciones\, las consecuencias de estos fallos son apenas perceptibles\, pero en otros ámbitos esos fallos no son asumibles</span>

<span style="color:#58585A">La solución a este problema se llama </span>  <span style="color:#58585A"> __Error Correcting Code__ </span>  <span style="color:#58585A"> \(ECC\)\, un código que tiene la capacidad de detectar y corregir errores de bit</span>

<span style="color:#58585A">La memoria ECC \(Error Correcting Code\) o código de corrección de errores es un tipo de memoria de ordenador que detecta y corrige los tipos más comunes de corrupción de datos de la memoria\.</span>

<span style="color:#58585A">El Rank contiene 8 bits de memoria adicionales\, lo que hace un total de 72 bits\.</span>

<span style="color:#58585A">El Rank en DDR5 contiene 2\*8 bits de memoria adicionales\, lo que hace un total de 80 bits\.</span>

<span style="color:#58585A">A medida que se procesan los datos\, la memoria ECC está constantemente analizando código con un algoritmo especial para detectar y corregir errores de memoria de un solo bit → \(</span>  _[código Hamming](https://es.wikipedia.org/wiki/C%C3%B3digo_Hamming)_  <span style="color:#58585A">\)</span>

<span style="color:#58585A">Se utiliza en servidores\, sitios con información sensible o cálculos complejos\.</span>

<span style="color:#58585A">Generalmente\, la memoria ECC es más cara y puede ser un poco más lenta que la memoria normal\.</span>

<span style="color:#58585A">Los demás componentes del sistema\, como la CPU y la placa base\, también deben ser compatibles con una memoria ECC\.</span>

_Cuando no está presente esta tecnología puede venir indicado como _  _Non\-ECC_  _\._

![](assets/img/Unidad05/Unidad542.png)

![](assets/img/Unidad05/Unidad543.png)

# 7. RAM Buffered/Registered

<span style="color:#000000">La Memoria RAM “Buffered” o Memoria “Registered” tiene un registro situado entre la DRAM y el Controlador de Memoria del Sistema\. Esto hace que haya menos carga eléctrica en el Controlador de Memoria y permite que sistemas con muchos módulos de memoria permanezcan estables\, de otra forma esto no sería posible\. </span>

<span style="color:#000000">Más cara de construir y utilizada en servidores\.</span>

<span style="color:#000000">Cuando se fabrica como un módulo de memoria dual en línea \(DIMM\)\, un módulo de memoria registrado se denomina RDIMM \, mientras que la memoria no registrada se denomina UDIMM o simplemente DIMM</span>

<span style="color:#222222">Cuando no poseen esta característica nos puede venir indicado como </span>  <span style="color:#222222"> _Unbuffered o Unregistered_ </span>  <span style="color:#222222">\.</span>

![](assets/img/Unidad05/Unidad544.png)

![](assets/img/Unidad05/Unidad545.png)

# 7. Perfiles

* <span style="color:#000000">La memoria está preparada para trabajar a diferentes frecuencias y diferentes latencias\. Cada configuración de frecuencias\, latencias y voltaje se conoce como perfil\, y el fabricante asegura que el rendimiento es óptimo con esos perfiles\. Estos perfiles se almacenan en el circuito SPD de la memoria\.</span>
* <span style="color:#000000">Existen dos tipos de perfiles\, dentro de cada tipo\, el fabricante puede configurar diferentes variantes\.</span>
* <span style="color:#000000">Perfiles JEDEC: son configuraciones aprobadas por el organismo encargado de la estandarización de la memoria RAM\. Estas configuraciones son muy seguras pero no aprovechan las altas frecuencias de las memorias RAM actuales\. Suelen venir indicadas con un número\, por ejemplo\, JEDEC \#4\, JEDEC \#5\, etc\.</span>
* <span style="color:#000000">Perfiles XMP \(Intel eXtreme Memory Performance\) o DOCP/EXPO \(AMD\): son configuraciones aprobadas por Intel</span>  y AMD  <span style="color:#000000">para conseguir obtener frecuencias de funcionamiento de la memoria superiores a las aprobadas por JEDEC\. Suelen venir indicadas con un número\, por ejemplo\, XMP\-3200\, XMP\-4000\, etc\.</span>
  * _[https://www\.asus\.com/latin/support/FAQ/1042256/](https://www.asus.com/latin/support/FAQ/1042256/)_
* <span style="color:#000000">Por defecto la placa base sólo funciona con perfiles JEDEC\, detectando automáticamente el perfil que mejor rendimiento tenga\. Si la placa base está preparada para admitir perfiles XMP o </span> DOCP/EXPO <span style="color:#000000">\, estos se podrán configurar desde la BIOS/</span> UEFI <span style="color:#000000">\.</span>

![](assets/img/Unidad05/Unidad546.png)

# 7. Identificación de RAM

_[https://www\.kingston\.com/spain/es/memory/memory\-part\-number\-decoder](https://www.kingston.com/spain/es/memory/memory-part-number-decoder)_  <span style="color:#000000"> </span>

# 7. Etiquetas

<span style="color:#000000"> __KVR32N22D8/16__ </span>  <span style="color:#000000"> \(</span>  _[http://www\.kingston\.com/dataSheets/KVR32N22D8\_16\.pdf](http://www.kingston.com/dataSheets/KVR32N22D8_16.pdf)_  <span style="color:#000000"> \)</span>

<span style="color:#000000">KVR\. Corresponde a las iniciales del fabricante \(Kingston\)</span>

<span style="color:#000000">32\. Corresponde a la velocidad efectiva en MHz \(3200MHz\)</span>

<span style="color:#000000">N\. NonECC \(No corrige errores\)\. Si fuera E \(ECC\) corrige errores\.</span>

<span style="color:#000000">22\. Latencia \(CAS\)\.</span>

<span style="color:#000000">D\. Dual Channel\. Si fuera S \(Single\)\, Q\(Quad\)</span>

<span style="color:#000000">8\. Número de chips de memoria\.</span>

<span style="color:#000000">16\. Capacidad del módulo \(16GB\)</span>

![](assets/img/Unidad05/Unidad547.png)

<span style="color:#000000"> __KVR16N11K2/16 __ </span>  <span style="color:#000000">\(</span>  _[http://www\.kingston\.com/dataSheets/KVR16N11K2\_16\.pdf](http://www.kingston.com/dataSheets/KVR16N11K2_16.pdf)_  <span style="color:#000000"> \)</span>

<span style="color:#000000">KVR\. Corresponde a las iniciales del fabricante \(Kingston\)</span>

<span style="color:#000000">16\. Corresponde a la velocidad efectiva en MHz \(1600MHz\)</span>

<span style="color:#000000">N\. NonECC \(No corrige errores\)\. Si fuera E \(ECC\) corrige errores\.</span>

<span style="color:#000000">11\. Latencia \(CAS\)\.</span>

<span style="color:#000000">K2\. Kit de 2 piezas</span>

<span style="color:#000000">16\. Capacidad del módulo \(16GB\)</span>

![](assets/img/Unidad05/Unidad548.png)

![](assets/img/Unidad05/Unidad549.png)

<span style="color:#000000"> __KVR26S19S8/16__ </span>  <span style="color:#000000"> \(</span>  _[http://www\.kingston\.com/dataSheets/KVR26S19S8\_16\.pdf](http://www.kingston.com/dataSheets/KVR26S19S8_16.pdf)_  <span style="color:#000000"> \)</span>

<span style="color:#000000">KVR\. Corresponde a las iniciales del fabricante \(Kingston\)</span>

<span style="color:#000000">26\. Corresponde a la velocidad efectiva en MHz \(2600MHz\)</span>

<span style="color:#000000">S\. Tipo de módulo SODIMM</span>

<span style="color:#000000">19\. Latencia \(CAS\)\.</span>

<span style="color:#000000">S\. SODIMM</span>

<span style="color:#000000">8\. Número de chips de memoria\.</span>

<span style="color:#000000">16\. Capacidad del módulo \(16GB\)</span>

<span style="color:#000000">CT32G4S266M \(</span>  _[https://www\.crucial\.es/memory/ddr4/ct32g4s266m](https://www.crucial.es/memory/ddr4/ct32g4s266m)_  <span style="color:#000000"> \)</span>

<span style="color:#000000">CT\. Crucial</span>

<span style="color:#000000">32G\. Capacidad del módulo \(32GB\)</span>

<span style="color:#000000">S\. SODIMM</span>

<span style="color:#000000">266\. Velocidad efectiva \(2666MHz\)</span>

<span style="color:#000000">M\. compatible con MAC</span>

![](assets/img/Unidad05/Unidad550.png)

<span style="color:#000000"> __CT32G4DFD8266__ </span>  <span style="color:#000000"> \(</span>  _[https://www\.crucial\.es/memory/ddr4/ct32g4dfd8266](https://www.crucial.es/memory/ddr4/ct32g4dfd8266)_  <span style="color:#000000"> \)</span>

<span style="color:#000000">CT\. Crucial</span>

<span style="color:#000000">32G\. Capacidad del módulo \(32GB\)</span>

<span style="color:#000000">4DF</span>

<span style="color:#000000">D8\. Dual Channel</span>

<span style="color:#000000">266\. Velocidad efectiva \(2666MHz\)</span>

<span style="color:#000000"> __CMK64GX4M4B3600C18 __ </span>  <span style="color:#000000">\(</span>  _[https://www\.corsair\.com/es/es/Categor%C3%ADas/Productos/Memoria/VENGEANCELPX/p/CMK64GX4M4B3600C18\#tab\-tech\-specs](https://www.corsair.com/es/es/Categor%C3%ADas/Productos/Memoria/VENGEANCELPX/p/CMK64GX4M4B3600C18#tab-tech-specs)_  <span style="color:#000000"> \)</span>

<span style="color:#000000">CMK\. Corsair</span>

<span style="color:#000000">64GX4M4\. Kit de 64 GB \(4x16GB cada uno\)</span>

<span style="color:#000000">3600\. Corresponde a la velocidad efectiva en MHz \(3600MHz\)</span>

<span style="color:#000000">18\. Latencia \(CAS\)\.</span>

![](assets/img/Unidad05/Unidad551.png)

# 7. ¿Cómo saber qué memoria tengo instalada?

<span style="color:#000000">¿Cómo saber qué memoria tengo instalada? Podemos usar software de terceros o acceder al símbolo de sistema \(Windows\+r→cmd→y ejecutar “wmic memorychip”</span>

![](assets/img/Unidad05/Unidad552.png)

# 8. VRAM

<span style="color:#58585A">Video Ram o memoria de vídeo está presente en todas las tarjetas gráficas\, es un tipo de memoria diseñada especialmente para llevar a cabo un tipo concreto de tareas en aplicaciones gráficas y videojuegos\.</span>

<span style="color:#58585A">GDDR SDRAM\, es el tipo de RAM de gráficos más popular\, y es lo que encontrará en la gran mayoría de las GPUs actuales\. La abreviatura significa Graphics Double Data Rate Synchronous Dynamic Random\-Access Memory</span>

![](assets/img/Unidad05/Unidad553.png)

![](assets/img/Unidad05/Unidad554.png)

<span style="color:#58585A">HBM\(High Bandwidth Memory\)\, tipo de memoria gráfica que tiene un ancho de banda mucho mayor que GDDR6\, alto coste \(HBM\, </span>  _[HBM2](https://www.pccomponentes.com/amd-radeon-pro-wx-9100-16gb-gddr5-hbm2)_  <span style="color:#58585A">\, </span>  _[HBM2E](https://hardzone.es/tutoriales/rendimiento/memoria-hbm2e-caracteristicas-especificaciones/)_  <span style="color:#58585A">\)</span>

# Bibliografia

_[https://computerhoy\.com/reportajes/tecnologia/latencia\-vs\-megahercios\-importante\-elegir\-ram\-pc\-420979](https://computerhoy.com/reportajes/tecnologia/latencia-vs-megahercios-importante-elegir-ram-pc-420979)_

_[https://computerhoy\.com/noticias/hardware/todo\-que\-necesitas\-saber\-memoria\-ram\-37541](https://computerhoy.com/noticias/hardware/todo-que-necesitas-saber-memoria-ram-37541)_

_[https://hardzone\.es/2018/01/17/asi\-funciona\-atencia\-memoria\-ram\-ddr4/](https://hardzone.es/2018/01/17/asi-funciona-atencia-memoria-ram-ddr4/)_  <span style="color:#000000"> </span>

_[https://www\.profesionalreview\.com/2018/07/21/latencia\-memoria\-ram/](https://www.profesionalreview.com/2018/07/21/latencia-memoria-ram/)_

_[https://www\.anandtech\.com/show/3851/everything\-you\-always\-wanted\-to\-know\-about\-sdram\-memory\-but\-were\-afraid\-to\-ask/2](https://www.anandtech.com/show/3851/everything-you-always-wanted-to-know-about-sdram-memory-but-were-afraid-to-ask/2)_  <span style="color:#000000"> </span>

_[https://hardzone\.es/2019/01/06/single\-rank\-vs\-dual\-rank\-amd\-ryzen/](https://hardzone.es/2019/01/06/single-rank-vs-dual-rank-amd-ryzen/)_  <span style="color:#000000"> </span>

_[https://hardzone\.es/tutoriales/componentes/tipos\-memoria\-ram\-pc\-historia/](https://hardzone.es/tutoriales/componentes/tipos-memoria-ram-pc-historia/)_

_[https://hardzone\.es/tutoriales/componentes/diferencias\-memoria\-ram\-ddr/](https://hardzone.es/tutoriales/componentes/diferencias-memoria-ram-ddr/)_

_[https://lau\-re\.wixsite\.com/laure/post/dimm\-vs\-so\-dimm\-hay\-diferencia\-de\-rendimiento](https://lau-re.wixsite.com/laure/post/dimm-vs-so-dimm-hay-diferencia-de-rendimiento)_

_[https://www\.ionos\.es/digitalguide/servidores/know\-how/memoria\-ecc\-almacenamiento\-seguro\-de\-datos/](https://www.ionos.es/digitalguide/servidores/know-how/memoria-ecc-almacenamiento-seguro-de-datos/)_  <span style="color:#000000"> </span>

_[https://infopcgamer\.com/gddr5\-vs\-gddr5x\-vs\-hbm\-vs\-hbm2\-vs\-gddr6/](https://infopcgamer.com/gddr5-vs-gddr5x-vs-hbm-vs-hbm2-vs-gddr6/)_  <span style="color:#000000"> </span>

_[https://hardzone\.es/reportajes/que\-es/vram\-tarjeta\-grafica/](https://hardzone.es/reportajes/que-es/vram-tarjeta-grafica/)_  <span style="color:#000000"> </span>

_[https://www\.ticarte\.com/contenido/especificaciones\-tecnicas\-de\-la\-memoria\-ram](https://www.ticarte.com/contenido/especificaciones-tecnicas-de-la-memoria-ram)_  <span style="color:#000000"> </span>
