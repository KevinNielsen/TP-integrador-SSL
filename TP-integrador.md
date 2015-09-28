#TP - Integrador
## **Alumno: Kevin Nielsen**
## *Curso K2051*

### Análisis Léxico
1.  Los digrafos y trigrafos son secuencias de dos y tres caracteres respectivamente, que aparecen en el código fuente.
	Según la especificación del lenguaje, este es remplazado por un único caracter.
	Se crearon por el hecho de que algunos teclados no tenian todos los caracteres necesarios para cubrir algunos lenguajes, o tambien porque algunos editores  tenian caracteres reservados para uso especial, etc.
2. Los trigrafos son reemplazados por el pre-procesador, en cambio, los digrafos son reemplazados en la tokenizacion.
3. 	**Lex 1:** int **Lex 2:** _ **Lex 3:** [ **Lex 4:** :> **Lex 5:** = **Lex 6:** <% **Lex 7:** - **Lex 8:** ! **Lex 9:** .0 **Lex 10:** , **Lex 11:** } **Lex 12:** ;
4. 	**int** array[]={-1,};
	**printf**("%d%d",**sizeof** array - **sizeof** array[0],**sizeof**(**char**)+array[0]);
	_Aclaración: Se cambio el nombre del vector de "_" a "array" para hacerlo mas legible_
5. Es correcta, ya que primero declara el prototipo de la funcion printf indicando que no tiene un numero fijo de parametros para pasarle (usando el ,... ).
   Luego hace la definicion de la funcion main, en la cual se declara una variable array de enteros,cuyo unico elemento es el 1. Reemplazando los digrafos podemos ver que los corchetes y llaves se cierran correctamente.

   
### Análisis Sintáctico
1. 
2. Es correcta, ya que es una UT + Decl. Externa (la primera vendria a ser la declaracion del array y en la 2da sería el uso de la funcion PrintF con dos argumentos)*



### Análisis Semántico
1. Es correcta semánticamente, ya que no viola ninguna restriccion semántica. Declara un arreglo de enteros y define por extensión sus elementos (en este caso uno solo, el -1 el cual es tambien int). Luego cuando utiliza la funcion _printf_, utiliza dos expresiones distintas en sus parámetros pero que ambas coinciden con el uso de la función _sizeof_, aunque se usan para diferentes cosas. En la primera se usa para saber el tamaño de un array y en la segunda expresión para saber el tamaño del tipo char. Ambos usos están aceptados en la definición de la función _sizeof_ así que es semánticamente correcto.
2. El programa primero declara el prototipo de la funcion _printf_, en donde dice que recibe N parametros.
	Luego, declara e inicializa un array de enteros, en el cual su unico elemento es el -1.
	Por ultimo utiliza la funcion _printf_, la cual imprime dos enteros decimales. En sus argumentos hay dos expresiones: 
	El 1er argumento se "subdivide" en 3 expresioness. Empezando por la expresion de la parte derecha, hace el _sizeof_ del elemento en la posicion 0 del array, lo cual devuelve 1. despues le resta al array el valor obtenido en la anterior expresion, con lo cual se resta una Posicion de memoria al array. Todo esto es el argumento que se le pasa a la funcion _sizeof_, que basicamente es lo mismo que tener _sizeof_ de un array vacio. El resultado final es, por lo tanto 0.
	El 2do argumento tiene una expresion (suma) pero se puede subdividir en dos, por un lado realiza el _sizeof_ del tipo de datos CHAR colocando los parentesis obligatorios para este caso. En la 2da expresion, se obtiene el elemento que esta en la posicion 0 del arreglo (esto es correcto ya que la suma es conmutativa y basicamente hace base del arreglo + posiciones de memoria). Por lo tanto la suma final es 1 + (-1) que da 0.
3. El resultado es 00. El primer cero, es el resultado de hacer el _sizeof_ de un array vacio (0 elementos). Y el segundo cero es el resultado de la suma entre el tamaño del tipo CHAR con el elemento en la primera posicion del array.