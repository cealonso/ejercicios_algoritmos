# EJERCICIOS SOBRE ALGORITMOS

### Ejercicio 1

Realizar un algoritmo que dado tres números permita obtener el mayor de los tres.

Ejemplo:
Dado los números: 10,30,5. Informar que el mayor es el número 30

    var num1=10;
    var num2=30;
    var num3=5;
    var max_valor=0;   
    
    if (num1>num2)
       max_valor=num1;
    else
       max_valor=num2;
    if (max_valor>num3)
       nuevo_max_valor=max_valor;
    else
       nuevo_max_valor=num3;
       
    console.log(nuevo_max_valor);
    
### Ejercicio 2

Realizar un algoritmo que permita saber si alcanza la cantidad de asientos disponibles para los 
participantes de un congreso de informática, para ello se conoce la cantidad de asistentes y la 
cantidad de asientos de dicho congreso. De faltar asientos indicar el número de asientos a 
agregar

### Ejercicio 3

Simular la función de autorrellenar de Microsoft Excel que permite completar otras celdas en 
base a un patrón numérico. Para ello se debe indicar en dos variables distintas cuales son los 
primeros números en que se va a basar el patrón (el segundo valor debe ser mayor que el 
primero), luego en base a esa diferencia se arma un bucle para completar las otras celdas. Para 
simplificar el proceso el bucle finaliza en el valor 10.
Ejemplo:
Para una serie como “1, 2, 3, 4, 5…”, el primer valor seria 1 y el segundo valor seria 2. Para la 
serie “2, 4, 6, 8…”, el primer valor seria 2 y el segundo 4

     var num1=prompt();
     var num2=prompt();
     num1=parseInt(num1);
     num2=parseInt(num2);
     var diferencia=num2-num1;
     console.log(num1);
     console.log(num2);
     
     for (var i=1;i<=10;i++){
           console.log(num2=num2+diferencia);
     }
     
### Ejercicio 4

Realizar una función denominada fill() que permita crear un nuevo array. La función tendrá dos 
parámetros. El parámetro array_size será un entero que indicará la cantidad de veces que tendrá
que agregar el valor del segundo parámetro denominado value al nuevo array.

Ejemplo:
console.log(fill(3,”a”)); 

Salida: [“a”, “a”, “a”]

    function fill(array_size, value){
    var arr_new=[];
    for(var i=1;i<=array_size;i++){
        arr_new.push(value);
        }
       return arr_new;
    }
    var num=prompt();
    var valor=prompt();
    var arr_completo=fill(num,valor);
    
 ### Ejercicio 5
 
Realizar un algoritmo donde el usuario (usr1) juegue contra la computadora (usr2) al juego piedra-papel-tijera. El resultado
del vencedor debe mostrarse por pantalla.
    
       /**
        * Compara dos valores (piedra-papel-tijera) para determinar que usuario ganó el juego.
        * 
        * @param  {string} choice1   valor piedra-papel-tijera del usuario 1
        * @param  {string} choice2   valor piedra-papel-tijera del usuario 2
        * @return  {string} result   mensaje con el usuario ganador
       */
      
        function compare(choice1, choice2) {
            let result = null;

            if (choice1 === choice2) {
                result = "Empate entre los jugadores";
            }

            if (choice1 === "piedra" && choice2 === "tijera") {
                result = "Gano usuario 1";
            }

            if (choice1 === "tijera" && choice2 === "papel") {
                result = "Gano usuario 1";
            }

            if (choice1 === "papel" && choice2 === "piedra") {
                result = "Gano usuario 1";
            }

            if (choice1 === "tijera" && choice2 === "piedra") {
                result = "Gano usuario 2";
            }

            if (choice1 === "papel" && choice2 === "tijera") {
                result = "Gano usuario 2";
            }

            if (choice1 === "piedra" && choice2 === "papel") {
                result = "Gano usuario 2";
            }

            return result;

        }

        function random(min, max) {
            return Math.floor((Math.random() * (max - min + 1)) + min);
        }

        var usr1 = prompt("Ingrese (piedra,papel o tijera): ");
        var arr = ["piedra", "papel", "tijera"];
        var numero = random(0, 2);
        var usr2 = arr[numero];
        console.log(usr1);
        console.log(usr2);
        console.log(compare(usr1, usr2));

### Ejercicio 6

Desarrolle un algoritmo que permita reemplazar los elementos de una lista de la siguiente manera:
Si el número de la lista es par reemplazar por la palabra manzana.
Si el número de la lista es impar reemplazar por la palabra pera.

Ejemplo:
[10, 0, -8, 1, 2, 90, 100, 5, 0, 0];

Devolvería:
[ "manzana", "manzana", "manzana", "pera", "manzana", "manzana", "manzana", "pera", "manzana", "manzana" ]

       
### Ejercicio 7

Realizar un algoritmo que dado dos números indicar si son números opuestos. Los números son opuestos cuando tienen el mismo módulo (es decir, están a la misma distancia desde el cero con signo contrario). Para realizar este algoritmo debe validarse que el primer número sea positivo y el segundo número sea negativo.

Ejemplo:

console.log(test(4,-4)) devuelve true.

console.log(test(8,-4)) devuelve false.

console.log(test(-6,-5)) devuelve false.

console.log(test(7,2)) devuelve false.

     function test(a,b){
             if ((a>0) && (b<0) && (a==(-1)*b)){
                 return true;
             }
             return false;
     }

      
