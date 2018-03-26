---
layout: post
title: "¿Endesa nos roba?"
image_small: "/assets/images/2013/endesa-647x231.jpg"
intro: >
    Repasando papeles me he tropezado con un folleto de publicidad de HC Energía
    que tenía pendiente de estudiar de cara a un posible ahorro en mis facturas
    del hogar. Me he llevado una sorpresa al mirar mi factura de electricidad.
date: 2013-02-15 19:23 0100
---
Pretendía comparar precios, nada más, y cuando me he puesto a hacer yo los cálculos que aparecen en la factura me he dado cuenta de un error, minúsculo e inocente en apariencia, que me ha hecho incluso pensar, por deformación profesional, en que los ingenieros que les han desarrollado la aplicación de facturación a la gente de Endesa no debían ser muy avispados.<!--more-->

Resulta que los redondeos de los importes están mal hechos. Aquí tenéis los cálculos de una de mis facturas:

[![Detalle de la factura de Endesa](/assets/images/2013/ENDESAFACTURA-DETALLE.png)](/assets/images/2013/ENDESAFACTURA-DETALLE.png)

A la hora de poner los precios de la tarifa se explayan con los decimales. Ahora bien, a la hora de hacer el cálculo no les han enseñado a redondear los resultados. Centrémonos en el consumo y el término de potencia, obviando los descuentos:

    5,75kW * 64 días * 0,059817€/kW-Dia = 22,012656€

Todo el mundo sabe que para redondear un número decimal se redondea de derecha a izquierda y se suele aumentar la cifra de la izquierda si la que quitamos es mayor que 5. Podríamos decir que en este caso el redondeo es el siguiente:

    22,012656
    22,01266
    22,0127
    22,013
    22,01

Pues bien, los señores de Endesa escriben en su lugar `22,02`, es decir, entre el resultado original con todos sus decimales y el que ellos escriben existe un error de `0,002656€`. Y entre el que nosotros escribiríamos y el que ellos escriben es de `0,01`, que es todavía más gordo.

Veamos ahora mi consumo:

    377kWh x 0,145578€/kWh = 54,882906€

En este caso el redondeo sería el siguiente:

    54,882906
    54,88291
    54,8829
    54,883
    54,88

También resulta curioso que en este caso, Endesa redondea el importe a `54,89€`. No son listos ni nada. En este caso, el error entre la cifra exacta y la escrita es de `0,002906€`, y entre lo que nosotros escribiríamos y lo que ellos escriben es, de nuevo (resulta obvio, por otro lado), `0,01€`.

En mi economia diaria la verdad es que esto no me afecta demasiado. De hecho, haciendo cálculos, no me importaría ni aunque yo viviese 100 años más, si el error se mantuviese en `0,02€` cada dos meses, ya que me estarían robando, 21% de IVA incluido:

    (0,02€ * 1,21) * 6 meses * 100 años = 14,52€

Tampoco nos vamos a poner en plan rácano.

Pero entonces me he preguntado: _¿Cuántos clientes tiene Endesa_ y claro, le he preguntado a [San Google](https://www.google.es/search?q=numero+clientes+endesa) y [el tercer resultado](http://www.endesa.com/ES/SALADEPRENSA/NOTICIAS/Nndesasuperalos25millonesdeclientesel%C3%A9ctricosentodoelmundo) me ha llevado a una página donde la gente del departamento de prensa de Endesa se jacta de que:

> Endesa supera los 25 millones de clientes eléctricos en todo el mundo de los cuales:
>
> 11,7 millones corresponden a España y Portugal

[![Captura de pantalla de la web de Endesa](/assets/images/2013/ENDESA2011.png)](/assets/images/2013/ENDESA2011.png)

Y si hacemos cálculos de repente los ingenieros de Endesa ya no te parecen tan despistados. Suponiendo que el número de clientes de Endesa en todo el mundo, que es más de 25 millones, es de 25 millones y un cliente, y que los errores de facturación de Endesa son más o menos iguales en todo el mundo, los cálculos le dejan a uno con cara de gilipollas.

**Cálculo utilizando el error exacto (factura bimestral)**

    Término de potencia: 0,002656 * 25.000.001 = 66.400,00€
    Consumo:             0,002906 * 25.000.001 = 72.650,00€
    -------------------------------------------------------
    Total bimestral:                            139.050,00€
    Total anual:                                834.300,00€

Es decir, en un año **Endesa podría estar ganando con un error tan tonto la friolera de 834.300€**.

**Cálculo utilizando el error computado en la factura (factura bimestral)**

    Término de potencia: 0,01 * 25.000.001 = 250.000,01€
    Consumo:             0,01 * 25.000.001 = 250.000,01€
    ----------------------------------------------------
    Total bimestral:                         500.000,02€
    Total anual:                           3.000.000,12€

Ahora si que lo vas a flipar: **3 millones de euros al año** _equivocándose_ en 2 céntimos al mes con cada uno de sus clientes en todo el mundo. Y esto con la factura de la luz. Con la del gas no he querido meterme.

Aquí tenéis mi factura completa, con los datos sensibles convenientemente ocultos:

[![Factura real de Endesa](/assets/images/2013/ENDESAFACTURA.png)](/assets/images/2013/ENDESAFACTURA.png)

Por supuesto, todo esto es una hipótesis. No pienso meterme en las cuentas de Endesa a buscar pufos. Si alguien quiere investigar, que lo haga. Por 15€ no me voy a mover, pero si os sentís muy indignados, podéis cambiar a un proveedor que sepa algo más de matemáticas.

* * *

**Edito:** Según el diario [Cinco Días](http://www.cincodias.com/articulo/empresas/beneficio-endesa-cae-46-2212-millones/20120229cdscdsemp_1/) en 2012 el beneficio de Endesa cayó un 46% y se quedó en 2.000 y pico millones. Con esas cifras me creo que haya podido descubrir un pufo de 3 millones al año.
