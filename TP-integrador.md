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
unidad-de-traducción
unidad-de-traducción declaración-externa 
declaración-externa definición-de-función
declaración especificadores-de-declaración declarador Proposición-compuesta
especificadores-de-declaración lista-de-declaradores-init especificador-de-tipo declarador-directo {Lista-declaraciones Lista-de-proposiciones}
especificador-de-tipo declarador-init int identificador (lista-tipos-de-parametro) {especificadores-de-declaración lista-declaradores-init ; Proposición-expresión}
int declarador int main (lista-de-parametros) { Especificador-de-tipo Declarador-init ; expresión ; }
int declarador-directo int main (declaración-parámetro)  { int Declarador= inicializador; Expresión-de-asignación ; }
int declarador-directo (lista-tipos-de-parametro) int main (especificadores-de-declaración) { int Declarador-directo [] = { Lista-de-inicializadores , } ; Expresión-condicional ; }
int identificador (lista-tipos-de-parametro) int main (especificador-de-tipo) { int identificador [] = { inicializador , } ; Expresión-lógica-OR ; }
int printf (lista-de-parametros, ...) int main (void)int main (void) { int _ [] = { Expresión-asignación , } ; Expresión-lógica-AND ; }
int printf (declaracion-parametro, ...) int main (void) { int _ [] = { Expresión-condicional , } ; Expresión-OR-inclusivo ; }
int printf (especificadores-de-declaración declarador, ...) int main (void) { int _ [] = { Expresión-lógica-OR , } ; Expresión-OR-exclusivo ; }
int printf (clasificador-de-tipo especificadores-de-declaracion declarador, ...) int main (void) { int _ [] = { Expresión-lógica-AND , } ; Expresión-AND ; }
int printf (const especificador-de-tipo declarador, ...) int main (void) { int _ [] = { Expresión-OR-inclusivo , } ; Expresión-de-igualdad ; }
int printf (const char apuntador declarador-directo, ..) int main (void) { int _ [] = { Expresión-OR-exclusivo , } ; Expresión-relacional ; }
int printf (const char * identificador, ...) int main (void) { int _ [] = { Expresión-AND , } ; Expresión-de-corrimiento ; }
int printf (const char *,...) int main (void) { int _ [] = { Expresión-de-igualdad , } ; Expresión-aditiva ; }
int printf (const char *,...) int main (void) { int _ [] = { Expresión-relacional , } ; Expresión-multiplicativa ; }
int printf (const char *,...) int main (void) { int _ [] = { Expresión-de-corrimiento , } ; Expresión-unaria ; }
int printf (const char *,...) int main (void) { int _ [] = { Expresión-aditiva , } ; Expresión-posfija ; }
int printf (const char *,...) int main (void) { int _ [] = { Expresión-multiplicativa , } ; Expresión-posfija ( Lista-de-expresiones-argumento) ; }
int printf (const char *,...) int main (void) { int _ [] = { Expresión-unaria , } ; Expresión-primaria ( Lista-de-expresiones-argumento, Expresión-asignación ) ; }
int printf (const char *,...) int main (void) { int _ [] = { Operador-unario Expresión-unaria, } ; identificador ( Lista-de-expresiones-argumento , Expresión-asignación, Expresión-asignación ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - Operador-unario Expresión-unaria , } ; printf ( Expresión-asignación , Expresión-asignación, Expresión-asignación ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! Expresión-posfija , } ; printf ( Expresión-condicional , Expresión-condicional, Expresión-condicional ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! Expresión-primaria , } ; printf ( Expresión-lógica-OR , Expresión-lógica-OR, Expresión-lógica-OR ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! constante , } ; printf ( Expresión-lógica-AND , Expresión-lógica-AND, Expresión-lógica-AND ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! Constante-flotante , } ; printf ( Expresión-OR-inclusivo , Expresión-OR-inclusivo, Expresión-OR-inclusivo ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-OR-exclusivo , Expresión-OR-exclusivo, Expresión-OR-exclusivo ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-AND , Expresión-AND, Expresión-AND ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-de-igualdad , Expresión-de-igualdad, Expresión-de-igualdad ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-relacional , Expresión-relacional, Expresión-relacional ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-de-corrimiento , Expresión-de-corrimiento, Expresión-de-corrimiento ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-aditiva , Expresión-aditiva, Expresión-aditiva ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-multiplicativa , Expresión-aditiva- Expresión-multiplicativa , Expresión-aditiva Expresión-multiplicativa) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-unaria , Expresión-multiplicativa- Expresión-unaria , Expresión-multiplicativa Expresión-unaria) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-posfija , Expresión-unaria- sizeof Expresión-unaria, Expresión-unaria Expresión-posfija) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-primaria , sizeof Expresión-unaria - sizeof Expresión-posfija, sizeof ( Nombre-de-tipo )  Expresión-posfija [ expresión ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( cadena , sizeof Expresión-posfija - sizeof Expresión-posfija [ expresión ] , sizeof ( char )  Expresión-primaria [ Expresión-asignación ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof Expresión-primaria - sizeof Expresión-primaria [ Expresión-asignación ] , sizeof ( char )  constante [ Expresión-condicional ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof identificador - sizeof identificador [ Expresión-condicional ] , sizeof ( char )  Constante-entera [ Expresión-lógica-OR ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-lógica-OR ] , sizeof ( char )  0 [ Expresión-lógica-AND ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-lógica-AND ] , sizeof ( char )  0 [ Expresión-OR-inclusivo ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-OR-inclusivo ] , sizeof ( char )  0 [ Expresión-OR-exclusivo ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-OR-exclusivo ] , sizeof ( char )  0 [ Expresión-AND ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-AND ] , sizeof ( char )  0 [ Expresión-de-igualdad ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-de-igualdad ] , sizeof ( char )  0 [ Expresión-relacional ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-relacional ] , sizeof ( char )  0 [ Expresión-de-corrimiento ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-de-corrimiento ] , sizeof ( char )  0 [ Expresión-aditiva ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-aditiva ] , sizeof ( char )  0 [ Expresión-multiplicativa ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-multiplicativa ] , sizeof ( char )  0 [ Expresión-unaria ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-unaria ] , sizeof ( char )  0 [ Expresión-posfija ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-posfija ] , sizeof ( char )  0 [ Expresión-primaria ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-primaria ] , sizeof ( char )  0 [ identificador ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ constante ] , sizeof ( char )  0 [ _ ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Constante-entera ] , sizeof ( char )  0 [ _ ] ) ; }
int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ 0 ] , sizeof ( char )  0 [ _ ] ) ; }
2. Es correcta, ya que es una UT + Decl. Externa (la primera vendria a ser la declaracion del array y en la 2da sería el uso de la funcion PrintF con dos argumentos)*



### Análisis Semántico
1. Es correcta semánticamente, ya que no viola ninguna restriccion semántica. Declara un arreglo de enteros y define por extensión sus elementos (en este caso uno solo, el -1 el cual es tambien int). Luego cuando utiliza la funcion _printf_, utiliza dos expresiones distintas en sus parámetros pero que ambas coinciden con el uso de la función _sizeof_, aunque se usan para diferentes cosas. En la primera se usa para saber el tamaño de un array y en la segunda expresión para saber el tamaño del tipo char. Ambos usos están aceptados en la definición de la función _sizeof_ así que es semánticamente correcto.
2. El programa primero declara el prototipo de la funcion _printf_, en donde dice que recibe N parametros.
	Luego, declara e inicializa un array de enteros, en el cual su unico elemento es el -1.
	Por ultimo utiliza la funcion _printf_, la cual imprime dos enteros decimales. En sus argumentos hay dos expresiones: 
	El 1er argumento se "subdivide" en 3 expresioness. Empezando por la expresion de la parte derecha, hace el _sizeof_ del elemento en la posicion 0 del array, lo cual devuelve 1. despues le resta al array el valor obtenido en la anterior expresion, con lo cual se resta una Posicion de memoria al array. Todo esto es el argumento que se le pasa a la funcion _sizeof_, que basicamente es lo mismo que tener _sizeof_ de un array vacio. El resultado final es, por lo tanto 0.
	El 2do argumento tiene una expresion (suma) pero se puede subdividir en dos, por un lado realiza el _sizeof_ del tipo de datos CHAR colocando los parentesis obligatorios para este caso. En la 2da expresion, se obtiene el elemento que esta en la posicion 0 del arreglo (esto es correcto ya que la suma es conmutativa y basicamente hace base del arreglo + posiciones de memoria). Por lo tanto la suma final es 1 + (-1) que da 0.
3. El resultado es 00. El primer cero, es el resultado de hacer el _sizeof_ de un array vacio (0 elementos). Y el segundo cero es el resultado de la suma entre el tamaño del tipo CHAR con el elemento en la primera posicion del array.