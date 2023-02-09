# Tabla de amortización

Created: 09-08-2022 17:57

## <span class="pink"> **Idea** </span>
Representan los datos relacionados con los pagos de un crédito.

Contienen información cómo la fecha a pagar, el monto, etc.

Actualmente existen tres tipos:

![[Tabla de amortización teórica.#span class pink Tabla teórica span]]

![[Tabla de amortización del cliente#span class pink Tabla del cliente span]]

![[Tabla de amortización contable#span class pink Tabla contable span]]

![[Pasted image 20220809175842.png]]

### ¿Cómo se genera?

Dentro del sistema de [[Resuelve/Abaco]] Se genera una estructura en la cuál se generan las fechas esperadas para el plazo dado. A esas fechas se les conoce cómo [[Cuotas]].

> [!example]
> 
Ejemplo: Si el crédito es de 12 meses, genera las 12 fechas en las que se debería realizar un pago

Al crear la estructura base de la tabla se va realizando una iteración sobre cada una de esas [[Cuotas]]. En cada iteración se calculan los campos de cada cuota, los cuales hacen referencia a el monto qué el cliente debe pagar,a sí cómo la administración de qué se hizo con el dinero del pago del cliente.

Con cada iteración para calcular las [[Cuotas]], se van calculando los campos correspondientes a la tabla Teórica.

Los cuales son:

* #### Balance
Es el monto total qué el cliente debe, considerando el monto solicitado en el crédito, seguro de vida y los demás rubros.

* #### Capital acumulado
Es el monto total pagado a la cantidad solicitada del crédito, sin considerar intereses ni otro rubro, es el pago únicamente del dinero qué se le dio al cliente.

* #### Suma de pagos
Es el total del dinero qué ha dado el cliente

* #### Intereses pendientes
Es el monto restante para liquidar el interés ordinario, es decir el interés qué genera una ganancia para Resuelve

* #### Interés moratorio pendiente
Es el monto restante para liquidar el interés moratorio, es decir el interés qué se genera cuándo el cliente se atrasa con los pagos.

* #### Interés sobre remuneración de servicios pendiente
Es el monto restante para liquidar el interés sobre remuneración de servicios, es decir el interés para pagar ese rubro.

* ![[Cuotas#span class pink Cuotas span]]

## <span class="orange"> **Tags**</span>
<span class="tag"> #visible</span> <span class="tag"> #build</span> <span class="tag"> #abaco</span> 

## <span class="green"> **References**</span>
<span class="blue"> **West: similar** </span>
<span class="blue"> **East: opposite** </span>
<span class="blue"> **North: theme/ question** </span>
[[Crédito]]
<span class="blue"> **South: what does this lead to** </span>
[[Tabla de amortización teórica.]]
[[Tabla de amortización teórica.]]
[[Tabla de amortización contable]]
[[Cuotas]]

### <span class="purple"> **Sources**</span>
1.  https://docs.google.com/spreadsheets/d/1iGk-qOsfwFz8EHEAyiyxUG7IuViTeC-smH-GEOkAqiI/edit#gid=513396406