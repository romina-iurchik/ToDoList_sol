## 404 - El readme se encuentra en construcción ⛏️🏗️🚧👷🏻‍♀️
<h1> ToDoList 🗒️</h1>   

## Descripción - Contrato que gestiona tareas, incluye:

- Estructura de la tarea:
  - descripción(cad de txt)
  - tiempo de creacion (entero)
- Array: s_tareas, almacena las tareas
- Eventos:
  - ToDoList_TareaAnidada
  - ToDoList_TareaCompletaYEliminada
- Funciones:
  - setTarea()
  - getTarea
  - eliminaTarea()
  - completarTarea()

## Tecnologías utilizas

- Solidity
- SPDX License Identifier: MIT
- Remix, VSC
- MetaMask

## Conceptos teóricos abordados

- Structs
- Asignación de datos
- Variables del tipo `uint`, `boolean` y `bytes32`
- Array
- Introducción alas variables globales
- Estructuras de control `condicional` y `bucle`
- Eventos
- Función Hash y Funciones ABI



## ¿Cómo usarlo?

- Te recomiendo pasar por la documentación en [mi primer contrato](https://github.com/romina-iurchik/Miprimercontrato) que explica como deployar el contrato en `Remix` 

## Apuntes o anotaciones de la clase que me ayudaron:
<h3>Tener en cuenta que son anotaciones personales que dependen algunas del contexto en el que se dijeron, no tomarlo literal e investigar un poquito.</h3>

- prag espacio Enter, autocompleta
- Las structs siempre empiezan con mayúscula por convención
- Cuando no se especifica la visibilidad de la variable por defecto es public
- Guardar en storage es mas costoso que guardar en memory. Calldata es la más barata de los tres pero no permite modificar.
- Analizando que bloque de código gasta más gas obteniendo el mismo resultado:
```
    Person memory aux;
    aux.name = _name;
    aux.id = _id;
    myInfoArray.push(aux);
    /*
        gas:     505427
        trxCost: 439501
        exeCost: 358191
    */

    myInfoArray.push(_name, _id)
    /*
        gas:     497495
        trxCost: 432604
        exeCost: 351784
    */
```
- En storage cosas que quiero guardar/persistir, memory calculos
- El block.timestamp es una variable global, cuando el minero ponga block.timestamp en un tx, tiene que definir el block.timestamp el cual tine que ser un valor especifico y posterior al último valor block.timestamp del bloque posterior.

<h2>Cierre:</h2>

- Si hay algo que esta mal o no entendes no dudes en mandarme mensaje
- Acepto modificaciones de formato/contenido
- Hecho con cariño como primeros pasos en el mundo de los contratos inteligentes 🎐