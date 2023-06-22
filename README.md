# taller10

## Problemática 1

En un juego de rol, se desea implementar un sistema de combate en el que participen diferentes tipos de personajes: guerreros, magos y arqueros. Cada personaje tiene atributos y habilidades únicas, así como diferentes métodos de ataque y defensa.

El objetivo del juego es enfrentar a los personajes en batallas y determinar el ganador en función de sus habilidades, estrategias y atributos. Los guerreros se destacan por su fuerza y habilidades cuerpo a cuerpo, los magos por sus hechizos y poderes mágicos, y los arqueros por su precisión y habilidades a distancia.

El sistema debe permitir crear nuevos personajes de cada tipo, asignarles atributos iniciales, como puntos de vida y nivel de experiencia, y permitirles subir de nivel a medida que ganan batallas. Además, se debe implementar un algoritmo de combate que evalúe las habilidades de cada personaje y determine el resultado de la batalla.

Utilizando programación orientada a objetos, herencia y polimorfismo, implementa el sistema de combate y las clases necesarias para representar a los diferentes tipos de personajes. Asegúrate de que cada tipo de personaje tenga sus propias habilidades y métodos de ataque y defensa, y que puedan interactuar entre sí en las batallas.

Para solucionar lo anterior se debe generar lo siguiente:

* Un diagrama exclusivo que involucren las funcionalidades principales del juego.
* Una solución en lenguaje de programación Java a través del IDE Netbeans. Usar Polimorfismo en la solución.
* Clase de prueba/ejecutor, que demuestre la funcionalidad del juego. 

### Análisis
Antes de comenzar con el desarrollo del sistema, es importante llevar a cabo un análisis profundo del problema y definir las funcionalidades principales del juego, así como las clases y métodos necesarios.

Funcionalidades principales:

1. Creación de personajes: El juego debe permitir a los jugadores crear personajes de los tres tipos: guerreros, magos y arqueros. Cada personaje deberá tener atributos iniciales únicos.

2. Batallas: Los personajes podrán enfrentarse en batallas. El resultado de cada batalla dependerá de las habilidades, estrategias y atributos de cada personaje.

3. Niveles: Los personajes podrán ganar experiencia y subir de nivel a medida que ganan batallas. Al subir de nivel, sus atributos mejorarán.

4. Habilidades: Cada tipo de personaje tendrá sus propias habilidades y métodos de ataque y defensa. Por ejemplo, los guerreros pueden tener habilidades de fuerza y resistencia, los magos pueden tener habilidades de magia y hechizos, y los arqueros pueden tener habilidades de precisión y distancia.

Clases necesarias:

1. Clase Personaje: Esta será la clase base que contenga los atributos y métodos comunes a todos los personajes, como puntos de vida, nivel de experiencia, ataque, defensa, y los métodos para obtener estos atributos y mejorarlos.

2. Clases Guerrero, Mago y Arquero: Estas clases heredarán de la clase Personaje e implementarán las habilidades y métodos de ataque y defensa específicos de cada tipo de personaje.

3. Clase Batalla: Esta clase se encargará de gestionar las batallas entre personajes. Incluirá un método para calcular el resultado de una batalla en función de las habilidades, estrategias y atributos de los personajes.

Diagrama de Clases:

La forma más sencilla de visualizar cómo se relacionan estas clases y funcionalidades es mediante un diagrama de clases UML, como el siguiente:

```
                         ----------------
                         |   Personaje   |
                         ----------------
                         | - vida        |
                         | - experiencia |
                         ----------------
                         | + atacar()    |
                         | + defender()  |
                         ----------------
                                /_\
                                 |
            -------------------------------------------------
            |                       |                       |
  -----------------       -----------------       -----------------
  |    Guerrero    |       |     Mago     |       |    Arquero    |
  -----------------       -----------------       -----------------
  | + fuerza       |       | + magia      |       | + precision   |
  -----------------       -----------------       -----------------
  | + atacar()     |       | + atacar()   |       | + atacar()    |
  | + defender()   |       | + defender() |       | + defender()  |
  -----------------       -----------------       -----------------
```

Este es un análisis inicial del problema, que sirve como base para el desarrollo del sistema de combate y la implementación de las clases en Java. En las siguientes etapas del desarrollo se detallarán los métodos y atributos de cada clase, y se implementará la lógica del juego.

## Problemática 2

En un restaurant se tiene diferentes tipos de menú para ofrecer a los clientes. Un cuenta por pagar está compuesta por características como: nombre del cliente, listado de todos las cartas(menú) solicitados por el cliente, valor a cancelar total,  subtotal, Iva.

Los tipos de menú del restaurant son:

**Menú a la Carta**

- nombre del plato
- valor del menú
* valor inicial del menú
* valor de porción de guarnición
* valor de bebida
* porcentaje adicional por servicio en relación del valor inicial del menú

**Menú del Día**

* nombre del plato
* valor del menú
* valor inicial del menú
* valor de postre
* valor de bebida


**Menú de Niños**

* nombre del plato
* valor del menú
* valor inicial del menú
* valor de porción de helado
* valor de porción de pastel

**Menú Económico**

* nombre del plato
* valor del menú
* valor inicial del menú
* porcentaje de descuento, en referencia al valor inicial del menú


Para solucionar lo anterior se debe generar lo siguiente:

* Un diagrama exclusivo que involucren las clases de tipo Menú (usar polimorfismo)
* Una solución en lenguaje de programación Java a través del IDE Netbeans. Usar Polimorfismo en la solución.
	* También debe existir en la solución un clase llamada Ejecutor001.java, donde conste el método main (**usar clase Ejecutor001**).
		* En dicho método se debe crear lo siguiente:
			*	Dos objetos de tipo menú de niños
			*	Un objeto de tipo menú de económico
			* Un objeto de tipo menú del día
			* Un objeto de tipo menú a la carta.
			*	Un objeto de tipo Cuenta (con datos iniciales como: nombre del cliente, IVA, listado de cartas -menú-, valor a cancelar total
			* Hacer uso del método toString para presentar toda la información posible del objeto Cuenta (nombre del cliente, subtotal, iva, listado de todos los menú, valor a cancelar a total.
	* Solucionar lo indicado en Ejecutor002.java

### Análisis
Para realizar un análisis adecuado, identificaremos los objetos clave (las clases que necesitamos) y cómo se relacionan entre sí.

**Clases principales y sus características:**

1. **Clase Menú:** Esta será nuestra clase base (superclase) que contendrá los atributos y métodos comunes a todos los tipos de menús, tales como nombre del plato y valor del menú.

2. **Clases Menú a la Carta, Menú del Día, Menú de Niños, Menú Económico:** Estas serán las subclases que heredan de la clase Menú. Cada una tendrá atributos y métodos adicionales según las características especificadas.

3. **Clase Cuenta:** Esta clase representará una cuenta por pagar. Contendrá el nombre del cliente, un listado de menús solicitados por el cliente, el valor total a cancelar, el subtotal y el IVA. Además, se implementará un método toString para presentar toda la información de la cuenta.

**Diagrama de clases UML para las clases de tipo Menú:**

```
             ----------------
             |     Menú     |
             ----------------
             | - nombrePlato|
             | - valorMenu  |
             ----------------
             | + getNombre()|
             | + getValor() |
             ----------------
                     /_\
                      |
     --------------------------------------
     |                 |                 |
----------------       |         ----------------
| Menú a la Carta|    ----------------    | Menú Económico |
----------------       | Menú del Día |    ----------------
| + valorPorcion |     ----------------    | + descuento    |
| + valorBebida  |                 |       ----------------
| + porcServicio |          ---------------- 
----------------          | Menú de Niños |
                          ----------------
                          | + valorHelado |
                          | + valorPastel |
                          ----------------
```

**Flujo básico del programa:**

En la clase `Ejecutor001`, se crearán diferentes objetos de los tipos de menús mencionados. Posteriormente, se creará un objeto `Cuenta` al que se le asignará un nombre de cliente, IVA y la lista de menús creados. Finalmente, se utilizará el método `toString` para presentar la información de la cuenta.

Este análisis preliminar proporciona un marco general para el desarrollo del sistema. En las siguientes etapas del desarrollo, se detallarán los métodos y atributos de cada clase, se implementará la lógica del programa y se realizarán las pruebas necesarias para garantizar que el sistema funciona según lo previsto.