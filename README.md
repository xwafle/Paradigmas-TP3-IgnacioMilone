# Paradigmas-TP2-IgnacioMilone-ExequielAlaniz-RamiroFernandez
TP1 De la materia paradigmas de programacion hecho por los alumnos de Ingenieria En Sistemas
- Exequiel Alaniz
- Ignacio Milone
- Ramiro Fernandez
  ## CONTENIDOS: 
  - EJERCICIO 1 (teoria sobre JavaScrypt orientado a objetos) ✔️
  - EJERCICIO 2 (Calculadora en TypeScrypt utilizando clases) ⏳
  - EJERCICIO 3 (ToDoList orientado a objetos) ✔️ (2.0)
  - EJERCICIO 4 (Explicacion y fundamento de lo que utilizamos en el codigo) ✔



## Ejercicio 1 - JS POO
  1. Generalización simbólica: ¿Cuáles son las reglas escritas del lenguaje? 
  
      **Respuesta:** Al aplicarlo al paradigma orientado a objetos las reglas simbolicas se centran en : Clases y objetos, encapsulaciones, herencias, polimorfismo y abstraccion
                    
  2. Creencias de los profesionales: ¿Qué características particulares del lenguaje se
  cree que sean "mejores" que en otros lenguajes?
  
      **Respuesta:** Se considera mas flexible al tener objetos y clases mas ligeros y dinamicos facilita la creacion de modelos y prototipos


## Ejercicio 4 - Explicacion y fundamentos

Para el ejercicio de la lista de tareas intentamos utilizar todas las caracteristicas de la POO, en primer lugar tenemos la **abstraccion** para poder expresar las caracteristicas de nuestro objeto Cargar (nombre a mejorar) y el **encapsulamiento**
agrupado todo en ese mismo objeto, esto hecho asi para solo tener que modificar (si es que hay que modificarlo) desde el modulo cargar.js y utilizando el metodo Cargar.Ingresar()

este mismo objeto es el que nos permite tambien tener **herencia** en nuestro programa ya que cada tarea que creamos con el metodo, hereda de Cargar todos sus atributos
``` js
export const Cargar = {
    titulo: "",
    descripcion: "",
    estado:"", 
    fechaVencimiento: "",
    dificultad: "",
    fechaActual: "",
    id: 0,
       Ingresar(){
            this.titulo = prompt("Ingrse el titulo de la tarea: ");
            this.descripcion = prompt("Ingrese la descripcion de la tarea (opcional): ") || "Sin descripcion";
            this.estado = prompt("Ingrese el estado de la tarea (pendiente, en curso, terminada) (por defecto: pendiente): ") || "Pendiente";
            this.fechaVencimiento = prompt("Ingrese la fecha de vencimiento (opcional) (formato: dd/mm/aaaa): ") || "Sin vencimiento";
            this.dificultad = prompt("Ingrese la dificultad (facil, media, dificil) (por defecto: facil): ") || "Facil";
            this.fechaActual = new Date();
            this.id = tareas.length + 1;
            
            console.log("Tarea agregada con exito");
        },
};
```
Nuestro codigo tambien posee **modularidad**, dividiendolo en tres archivos independientes cada uno con su responsabilidad 
- index.js -> Es el programa principal donde se conectan todos los modulos
- Cargar.js -> Aca definimos el prototipo y el objeto cargar, encargado de la creacion de tareas
- Mostrar.js -> Contiene las funciones para visualizar, buscar y editar las tareas, asi como dos funciones para mostrar un menu especifico

Nuestro codigo **NO** cuenta con **polimorfismo**, esto se debe a que cuando utilizamos el metodo Ingresar() para crear objetos todos estos se comportan igual (aunque algunos tengan valores distintos es decir, puedo tener tareas sin fechas de vencimiento y otras que si) 
asi que al no tener que crear objetos que se comporten de manera distinta este codigo no utiliza polimorfismo









