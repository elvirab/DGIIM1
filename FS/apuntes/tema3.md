lenguajes : en base a

#Lenguajes de primera generación
No cambiamos nada, le ponemos nombre que nos recuerde que es lo que hace una instrucciojn

1.Lenguajes máquina: binario -->código de instrucciones  | operandos
 

Lo habitual es que para una vez se hacen máquinas que hacen refe

2. Lenguaje ensambrador:
en lugar de escrinir en binario, a cada parte se le asigna un símbolo
ENSAMBLADOR : Símbolos en el operando para quitar los 0 y los unos se tiene otra relación en una tabla, con los nombre que sonotro queramos (en principio) , esa tabla no la trae el se construye y tiene alguna restricción (que empiece por letra TABLA DE SÍMBOLOS, (recordar mapa de los ejejcutables) 
para construir ensamblador (se tiene directoria máquina, a cada una le corresponde un código binario, a esto se e asigna un nombre ejemlo
Repertorio 
LOAd es el 001101010 (inventado9 se e asigna nombre corto
 STARD 010101001
 ADD
 Esto se hace por tablas, si coincide el nombre va a por ella

La traduccuion de ensamblador a maquen en tablas de emsamblador con la se símbolos (la variables) creadas por el programador

---
# Segunda generación de lenguajes
3. MACRO ENSAMBLADORES
(MACRO secuencia de órdenes ordenadas) Hay determinada secuencias de instrucciones que se repoiten con frecuencia, se empaqueta y se hace macro
macro ensamlador: repertorio y otra serie de macros, el traductor de un macro ensamblador se le asignna un nombre que se busca en la tabla y te dará una lista de instrucciones.

# Tercera generación de lenguajes 51-52

El problema no era diseñar el lenguaje, sino el traductor y que una persona a papel no lo hiciera mejor, el lenguaje para el que hacen un compilador eficicente FORTRAN 1957 John Backns, (un compilador es un traductor, pero el traductor puede ser compilador o intérprete ) el lenguaje de control del sistema operativo es interpretado, estsoo no te generan ningún fichero.

Estos lenguajes son de "ALTO NIVEL", lo que hacien (lenguaje de sóimbolos) que incorporaban estructura en :
##### datos: estructuras, valores agrupaos que se pueden reconocer, ejemplos que : array, string, struct (tipo regsistro), con esto aparece la idea de tipo de dato: fichero, array, entero....
  - **primitivos**: el entero el real, naturales que permite manejar la máquina física: char, int, real  EL LENGUAJE LO CONOCE TODO
  - estructurados: tinen alguna estrucutura en base de primitivos : CONOCE MACROSCÓPICAMENTE LA ESTRUCTURA. del género lo conoce, pero tienei que afinarlo, tines que decir los campos que tiene y com afinarlo,
    - aparece la idea de expresión: (a+b)*f, esto antes no se podía hcer con macro ensambladores,
    - CONTROL DE FLUJO: en repertorio máquina lo que hacía que hacer era el acumulador o la dirección de memoria
      - if
      - bucles definido (en los 70 indefinido)
  (más tarde: - TDA tipos de datos abstractos, el lenguaje no conoce ni la estructura, ni el lenga)
Con esto aparecen dos tipos de sentencias (una sentencia es una ordden) 
- semanticamente simples : su signifiado solo depende de ella y de nada más, ejemplo una asignación , operación de entradas y salida de una sola variabe
- semánticamente compuestas, en esamblador no hay otra, una sentencia se ejecuta, y otra igual, en macro emsamblador, en alto nivel apareccen los dos, 
se formaliza tipo como terna tipo (G géreno (tipo, conjunto valores posoble, cómo se representan vg complemetat a uno o a dos) , Operaciones , Propiedads)  (GOP) ejemplo
int
- género: desde {-2 elevado aknl , 2 elecakjd}
- operacones susma rect
- propiedades : communtativa...
- **lo estructurado**s, array, ficheros, lo que conoce el lenguaje es la estrucutura del tipo èro no la composición (género), ejemplo array:
conoce el tipo de filas y columnas, luego abría que dar el tipo de dato, los valores primitivos con los que trabaja, lo que define el programador es el género,  género del tipo al que poertenece un vecor es por ejmplo R^3, pero no se puede multipliar un array con un array, las operaciones predefinidas no son para las matrices. SU GÉNERO Y OPERCIONES SON es una tabla de género, su género será {0, 1, 2} -> R a cada uno de sus elemento se le asigna un género.

Lo que tienen es que manipula una estrucutra ordenada como matrices pero se trabaja de manera individual, accediendo a ellos con una applicaciones
 El tipo establece la representación, en un array a representaciń de ese tipo de tres componentes de tipo real le asigna una dirección de memoria, y a partir de esa dirección de memoria que le asigne reservará espcacio para tres.
- instruciones: construiir sentencia de alto de nivel que haga de macro

#### Sentencias:
- expresiones: 
- sentencias compuestas: Esto influye en la ruptura del flujo, sentencias : leer, escribir, asignación, condicionals, bucles definidos, e indefinidos (while)
  - secuencias semáticamentes simple de una variable, las otras condicionas son semánticamente simples, con la sentencia de asignación, a = expresión, eso se corresponde con carga *load* b y lo almacenas en b (en a = b ) si es una expresion más compleja la única que se asemeja es la anterior, el compilador  el traductor se encara solo de la última,
  si tengo la instrucciń leer a, b , c , d, esto lo que hace el leer a , leer b , leer c... el paso a un nivel de alto nive es desarrollar el nivepl de machro nivel, esas instrucciones fijas son comon n patrón ,
  ^``` if expr the ```,
  un bucle definido tiene tiene teres expresiones: la incial, el final y el incremento, la semántica dle for es: ejecuta el cuerpo tal número de veces, un determinao número de veces, determinado antes de entrar, eso se hace con la expresion final - inicial divido entre el incremento. Para implemtarlo, se calcula un nḿeor entero ((la repeticiones) crea una variable menor que eso, pregunta si es menor, si los es ejecuta el cuerpo se recta uno y si sigue siendo meno se vuelve a repetir, SEMÁNTICA DLE FOR, hay comppiladores que lo ue hacen es calcular el número, si hacemos referencia a la variaboe asociada dommy variable, variable ficticia, si solo aparece ahí ahiu compiladores que ni la pones en la tabla de signo, si se utiliza en otro sitio ni la cambia, otros en cambio si que lo emplementa, pero en teoría no es la semántca ni lo que tienen que hacer, en otro no le asignab valores, a no ser que se utiloce dentro del cuerpo. SEMÁNTICA, EJECUTA EL CUERPO TAL NÚMEOR DE VECES.


### Definición de la gramática
Para definir lenguaje se necesita solo y exclusivamente esto: 
- vocabulao: cujjunto de palabras, lexco, reglas para construir lexñico
- diccionario: le asigna un significado a cada palara, significado atómico, su signifiaco no depende de otra, (sin incluir eto)
- gramatica define un aestrucutura, o más , estruccutia sintáctica, --> estructura semantica y se asocian significados, lo idea es que la sintactica cuincida cn la semántica.
- para obtener significado de conjunto de palabras se analizan inidivida y su estructuta y se construye significado concreto. 
 - Depende del contexto,
 - preciso y conciso
 - sin ambigúedad
 ---
 En los lenguajes de programación, definida de gramaica forma:  palacreas y estructutras
 simbulos de la cuadrpla:
 gramatica sol cuerpo, sin sgnifiacao
 - los singnos terminales son las palabras, tinee estructura, le asoscio significado atómico.
 - lso no terminales son los que se construyen a partir de palabras: frases, oraciones... definen estrucutras, tienen alguna estructura en la que intervienen signos terminales y no termianles, como tienen estructura habrá reglas para conformarla, **regplas de producción**

para eliminar la abguedad sintactica, cada elemeto no terminal, tenga una sola estructuta, las forma de que cada elememto no terminal es que tengan forma de árbol, de toda la forma que cuando yo vaya a entedet todo esto converegue a la raíz, que ese es el símbolo inicial de la gramática.

Si lo que se hace es generar frases, se genera tood el ´arbol.

dada la gramatica
flecha derecha estrutura simbolo no terminal izq simolo termian, , alternativas: barra vertica  ,

la e y la o no son terminal, sin estructura, con una regla de producción que define su estructula, uno o puede ser una o un por  n mas , menos, expresión una E opert¡dad con o una expresión enre parenteses, y la id identificador, un nobre de lo que sea, a partit sde esa grapatia se pede generar árboles,
ña estructura es vn, se coge la frase, se lee de izquierda a drecha, se ve si hay aguna regla de la gramática que reconozca a id, se coge una expresión,  deeb ser sintácticamente y gramanticamente corrector gracias a la regla semántica.
Aparte de la propriedad de condiciones el "if" es también ambiguo.

En la gramática hay como cuatro pisos;

Gramática libres <-- Máquina de Turing 
----------
GSC Gramatica sensible contexto
----------
Gramaticas independientres del contexto GIC <-- automatas con pila  --> sintaxis (gramatias en medio: gramarra con argmentos y gramtica a dos niveles o de Van W)
----------
gramatica regular o expresiones regulares <-- reconocidad por -- automatas finitos | especifica ---> lesicp
----------


- la gramátuca regular, tiene las palabras que utilizas en el sistema: ejmplos: nombre de fuciones, procedimientos,constantes, su declaración está reglado;
- Gramáticas independientes del contexto, para analizar, enteder y tratarla son las gramáticas independientes del contex, los lenguajes de programación, sus sentencias son independientes del contexto.
- Gramatias sensibles al contexto, ejemplo, lenguajes naturales (sujeto omito),  ejemplo reconicimento de voz
- Gramáticas libres, se diferencian de las anteriores por la reflas de produccuón. ejmplo en la realizaciín de un programa se define una gramarica linre, independientemente el algoritmo.

para expecificar la sintaxis, cómo escribimos los lexemas y las indipendientes del contexto,
Primero se unifica la gramática, falta el automáta ue los resuelva,

Autómata que lo lo que va reconociendo lo almacena en la pila o plo que le queda por reconocer

Máquina de turing, especifica qué es un algoritmo.

Para cada tipo de gramática creo la máqina y ya tengo hecho prácticamente el traductor

GRAMATICA CON ATRUBUTOS
las que mas se utilizas soon las gramatias con atributos, para expecificar las gramáticas de los lenguajes de programación.
Se construyen, se parte de gramática independiente dle contexto (uso particular en lenguajes de programación, la sacó ET IRONS),
cuadrupla ( GIC, A, E , C )
GIC: semántica básica, lenguaje de programación
atributo: en conjunto con su valor
reglas evalucación atributo, cómo asignar vlaor a esos atributos
condiciones: condiciones sobre los valores que puede tomar cada atriuto

Ejemplo Gramatia con atributos para expecificar las variables enteras:
- Se define los dígitos: 0123456789 (son caracteres ascci)
- cnstante entera: o un dígio o una constante seguida de un dígitos, ( es recursiva pro la izquierda, loo definido aparece en la definicióne)
- Símbolos terminales: el 01234567889, no terminales dígitos y constantes,y calor)

Atributos que tienen las constantes: el valor,
definimos atributo que sea valor le asignamos significado a los dígitos, a o como dígito le damos un valor 0, que resultas ser el valos de memoria
valro(1)=1; en memroia 000000000000000001
...
valor(9)=9;

donde he definido las constantes enteras, la regla de evalución serña valor(cnt) = valro dñigito
y como es recursiva, deberemos tener en cuenta la posición del dígito.
Finalmente, habría que tener la condición de valor máxima para evitar desbordamientos, pero esto se lo tengo que poner a la cosntante

SALE PARA EXPECIFICAR LA SEMÁNTICA DE LOS LENGUAES DE PROGRAMACIÓN, SE COSNTRUYE LA GRAMÁTIA CON ATRIBUTO, QUE SOLO EXPECIFICA SINTAXIS, DE UN LENGUAE QUE TIENE ALGO DE SENSIBILAD AL CONTEXTO, ME LA SALE LA EXPECFICACIÓN DEL LENGAE DE PROGRMACIÓN. 

Gramática:
<letras>a b c d e...z
<dígitos> 0123456789
<letra digitos> <letras|dígitos>
<identificadores> ---> <letras>|identificadores><letras dígitos>

Uns secuenza correcta de caracteres se llama *lexema*, unidad mínima de significado.
Cuando se pasa de las palabras al ámbito de las frases, las reglas sintáxticas,  En los leguanjes de programación cuando se pasa la palra, término concreto se pasa a n término genérico
término concreto -- se abstrae--> *token*
estructuras sintáxticas se representan en términos de token. (ejmplo en sintaxis un token sería sujeto, verbo, "pepe" lexema que sería sandía come")  
### Qué hace un compilador  
1.El compilado rlee caracteres y comprueba con la gramática  
juan := pepe +  10
id       id  op  cte
lee la j es una letra, continua puesto que puede ser
...
llega al espacio: elemento terminal
:= *separador* sentencia asignación a lo de derecha le asigna lo de la izquierda 
...
4Sentencia d eizquiedra a derecah hasta que encuentra un separador, localiza un lexema,   

Cnstruye tabla símbolos   
lexema  | tipo | longitud | dirección | otras | valor | otras 
--- 	| ---  | --- 	  | ---       | ---   | ---   | --- 
juan	| int  | 16 BITS  | 0 	      | aksdak| si se le asignado, si se ah inicializzdo | dkanvjf 
Pepe 	| real | 32 	  | 16 	      | akjfd | ad    | aldk 
j 	|kajfd | 112	  | 48 	      | akcd  | asmc  | almcdk  
10 	| int  | klaJSº	   |ALK	      |ADLK   | 10    |AKNL  

variales explicitas le asocia el tipo 
en las constantes tipo 10 le asingan implícitamente, el compilador le asicia un valos, ejemplo 10.

Cando se leen un progrma lo primero que aparee es una zona de declaraciones, qué es lo que voy a utilizar, le dice al compilador que ese ombre lo ienen que buscar en un determinado tipo, 

en la parte procedural cuando no se ha declaraod una variable, 
las direcciones son el signidiado del lexema; 

cuando ve un lexema si es correcto lo conoce como un token, identificador,                           
... cuntinua leyendo , pepe, ve    que es correcto porque se ha declarado  , identificador al sitáxtico, 
ver que una frase es correcta y añadir a tabla de símbilos     
>> la funciones son abstraciiones de sentencias, unn procedimiento es una abatreación de setiencia void, un procedimineto no devuelve valor
---
el identificador de variable lo que hace es iniciar una un nuevo lexema, sentecián de asignación, porque ya ha enviado la otra,  
Si se empieza un if empiez una sentencia condicional, a no ser que se ponga if := expresión, igual que for, while, llamadas a porcedimiento 
lo que expera después del := es una expresión (recordar árbol sintáctico), se va reconociendo hasta que se ve una expresión que es correcta y dice que eso es una sentencia correcta, así se haría el análisis sintaxtico.  

#### tipos de aŕboles sintaxticos   
##### De forma descendente   LL (letf left)
axioma  --> se hace descendentemente ( se supone correcta y se empiez a leer de arriba bajo) y de izquierda a derecha l 
          *
 iden		expr
		id  id

tiene una pla con lo que va analizando y guardanto ( esto el construtps )
#### LR 
Autómata más complejo qeu el anterior pero más eficiente 
lee hacia arriba de derecha a izquierda  

> en los libros tem ponen ll(n) o lr(n) siendo n el número de token que se le tineen que enviar par que la reconozca unívocamene 
> sobre una grrmatica de más de uno se puede trabajar con una de ll(1) o lr( 1) compactando los símbolos 

Resumen: 
lee caracter a caracter de izquierda a derecha, la anota o consuta en TS, recocn0oce token y se lo manda al analizador sintáctico que lo reconoce, con las familias LR y LL