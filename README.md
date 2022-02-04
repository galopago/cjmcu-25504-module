# AYUDA PARA MODULO CJMCU-25504

El modulo CJMCU-25504 basado en el circuito integrado de cosechamiento de energia BQ25504, tiene incorporados todos los componentes externos necesarios para usarlo. La configuracion de los diferentes parametros de este integrado se realiza mediante resistores, sinembargo la serigrafia no es clara, lo que hace dificil identificuar cual componente es cual. Adicional a esto, el fabricante del modulo usa unas etiquetas diferentes a las que usa el fabricante del integrado lo cual aumenta mas la confusion.

Este documento pretende presentar las equivalencias entre las etiquetas usadas por el fabricante del modulo tanto en el [esquematico](/assets/pdf/CJMCU-25504-SCHEMATIC.pdf) como en el pcb, con las expuestas por el fabricante del integrado en su [hoja de datos](/assets/pdf/bq25504.pdf). De esta forma sera mucho mas facil realizar cambios a los componentes para ajustarlo a nuestras propias necesidades

## El modulo en cuestion

La unica marca visible en el circuito impreso es CJMCU-25504, no hay referencias visibles al fabricante. La serigrafia de los componentes es dificil de leer.

![MODULE](/assets/img/CJMCU-25504-MODULE.png)

## Mapa de resistores

El siguiente grafico muestra visualmente cada uno de los resistores, con el nombre de la etiqueta como la usa el fabricante, y con el nombre de la etiqueta que uso el fabricante del modulo.

![MODULE](/assets/img/CJMCU-25504-RESISTORS.svg)

## Mapa de conectores
El siguiente grafico muestra visualmente cada uno de los conector, con el nombre de la etiqueta como la usa el fabricante, y con el nombre de la etiqueta que uso el fabricante del modulo. 

![MODULE](/assets/img/CJMCU-25504-PINOUT.svg)

Algo curioso en este modulo, es que el fabricante decidio no conectar directamente el divisor de voltaje que configura el MPPT al pin VOC_SAMP, sino que tanto el punto medio del divisor, como el pin VOC_SAMP se encuentran en el header, de forma tal que se puede optar por configurar el MPPT o deshabilitarlo mediante un puente.

MPPT

| TI ID | PCB ID | MARK | VALUE  |
|-------|--------|------|--------|
| ROC2  |  R2    | 63E  | 4.42 M |
| ROC1  |  R10   | 565  | 5.60 M |
| ROC1a |  R1    | 106  | 10.0 M |


OVERVOLTAGE

| TI ID | PCB ID | MARK | VALUE  |
|-------|--------|------|--------|
| ROV2  |  R4    | 59E  | 4.02 M |
| ROV1  |  R3    | 75E  | 5.90 M |
| ROV1a |  R14   | 0    |    0 M |

UNDERVOLTAGE

| TI ID | PCB ID | MARK | VALUE  |
|-------|--------|------|--------|
| RUV2  |  R6    | 61E  | 4.22 M |
| RUV1  |  R5    | 565  | 5.60 M |
| RUV1a |  R15   | 0    |    0 M |

VOLTAGE OK

| TI ID | PCB ID | MARK | VALUE  |
|-------|--------|------|--------|
| ROK3  |  R7    | 16E  | 1.43 M |
| ROK2  |  R9    | 61E  | 4.22 M |
| ROK1  |  R8    | 63E  | 4.42 M |
| ROK1a |  R16   | 0    |    0 M |

OVERTEMPERATURE

| TI ID       | PCB ID | MARK | VALUE |
|-------------|--------|------|-------|
| OT_PROG 60  |  R12   | 0    |   0 M |
| OT_PROG 120 |  R11   | N/A  |   N/A |

