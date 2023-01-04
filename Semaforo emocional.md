
Created: 03-01-2023 21:38

## <span class="pink"> **Idea** </span>
Es un menú que permite indicar información sobre el cliente, existen varios posibles atributos incluyendo sub menus que dependen del status, los valores aceptados son los siguientes:

> [!Diagrama de status]-
> ![[Pasted image 20230103220202.png]]


Para implementar la solución, al cargar la live view, desde el backed se detectará el status del crédito. 
Dependiendo del valor del status del crédito, se devolverá una lista con las posibles opciones a escoger, con base al diagrama de arriba.

El backend devolverá los posibles status en el socket bajo el nombre de `semaphore_states`.  Por otra parte el front, deberá guardar el valor seleccionado en la variable llamada `semaphore_status`.

En caso de que una de las opciones seleccionadas sea un sub menu, entonces al seleccionarlo el backend actualizara la lista de `semaphore_states` para dar los valores del sub menu.

Por otra parte, existirán dos botones, uno para guardar y otro para reiniciar el status.

La forma en la que interactuaran el front y el back será de la siguiente manera123:

``` mermaid
sequenceDiagram

Backend->>+Front: @semaphore_states

Front->>+Backend: @client_status

Front->>+Backend: @semaphore_status

Backend->>+Front: @semaphore_states

Front->>+Backend: @semaphore_status
```

La manera en la que se determinará el status del semaforo, será la siguiente:

```mermaid
graph TD

A[Semaforo emocional] -->B(Obtener status del crédito)

B --> C(Devuelve al front las opciones para ese status)

C --> D{Es un submenu?}

D --> |Sí| C

D --> |No| E(Guarda ese status en memoria)

E --> F{Se presiono el botón guardar?}

F --> |Sí| G(Se guarda el status del semaforo en la base de datos)

F --> |No| H(Se espera a que se presione el botón guardar o a que se cambie el status)
```

## <span class="orange"> **Tags**</span>
<span class="tag"> #visible</span> <span class="tag"> #abaco</span>

## <span class="green"> **References**</span>
<span class="blue"> **West: similar** </span>
<span class="blue"> **East: opposite** </span>
<span class="blue"> **North: theme/ question** </span>
<span class="blue"> **South: what does this lead to** </span>

### <span class="purple"> **Sources**</span>
1. 