# Java_Fundamentos
Bases del lenguaje Java
## Mi primer "Hola mundo" en Java
```Java
public class Saludo {
    public static void main(String[] args) {
        System.out.println("Hola Mundo");
    }
}
```
## Variables en Java
```Java
public class Variables {
    public static void main(String[] args) {
        // Cadena de caracteres
        String Nombre = "Bienvenido a Java edu";
        // Enteros
        int edad = 25;
        // Dobles
        double numeroDouble = 3.1415;
        // Caracter
        char letra = 'e';
        // Booleano
        boolean isStudent = true; // true or false
        // Flotante
        float numeroPii = 3.1415F;
        
        System.out.println(Nombre); // Bienvenido a Java edu
        System.out.println(edad); // 25
        System.out.println(numeroDouble); // 3.1415
        System.out.println(letra); // e
        System.out.println(isStudent); // true
        System.out.println(numeroPii); // 3.1415
    }
}
```
## Concatenación
```Java
public class Concatenacion {
    public static void main(String[] args) {
        String nombre = "Edu";
        String apellido = "Casanas";
        int calificacion = 8;
        String materia1 = "python", materia2 = "swift";
        String materias = materia1 + " " + materia2;

        System.out.println(nombre + " " + apellido); // Edu Casanas
        System.out.println("Mi nombre es: " + nombre); // Mi nombre es: Edu
        System.out.println("Mi calificacion es: " + calificacion); // Mi calificacion es: 8
        System.out.println(materias); // python swift
        System.out.println(nombre.concat(" ").concat(apellido)); // Edu Casanas
    }
}
```
## Tipo de variable: VAR
```Java
public class Var_Java {
    public static void main(String[] args) {
        // var intuye el tipo de dato, para ello, var necesita inicializarse primero.
        var nombre = "educasanas";
        var edad = 23;
        var medidasCasa = 23.54;

        System.out.println(nombre); // educasanas
        System.out.println(edad); // 23
        System.out.println(medidasCasa); // 23.54
    }
}
```
## Comentarios
```Java
public class Comentarios {
    public static void main(String[] args) {
        // este codigo no se ejecuta ya que es un comentario.

        /*
        Este es un comentario multilinea que no se ejecutara.
         */
    }
}
```
## Ingresar datos
```Java
import java.util.Scanner;

public class Input_Datos {
    public static void main(String[] args) {
        String nombre;
        int edad;

        // Ingreso de datos
        Scanner entrada = new Scanner(System.in);

        System.out.println("Escribe tu nombre: ");
        nombre = entrada.next();

        System.out.println("Escribe tu edad: ");
        edad = entrada.nextInt();

        // Salida de datos
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
    }
}
```
## Ingresar datos 2 forma "Interfaz grafica"
```Java
import javax.swing.*;

public class Input_datos2 {
    public static void main(String[] args) {
        String nombre;
        int edad;

        // ingreso de datos
        nombre = JOptionPane.showInputDialog(null, "Ingrese su nombre: ");
        // JOptionPane.. solo maneja strings por eso creamos otra variable tipo string
        String edad2 = JOptionPane.showInputDialog(null, "Ingrese su edad: ");
        // Una vez recibido el valor como 'string', lo convertimos a entero.
        edad = Integer.parseInt(edad2);

        // mostrar datos
        JOptionPane.showMessageDialog(null, "Nombre: " + nombre + "\n" +
                                                                        "Edad: " + edad);
    }
}
```
## Casting
```Java
public class Casting {
    public static void main(String[] args) {

        // de texto a entero
        String numeroTexto = "123";
        int numeroEntero = Integer.parseInt(numeroTexto);

        System.out.println("Numero entero: " + numeroEntero*2); // 246

        // entero a texto
        int numeroEnteroAtexto = 123;
        String enteroToText = String.valueOf(numeroEnteroAtexto);

        System.out.println("El numero en string es: " + enteroToText); // "123"

        // double a entero
        double numeroDouble = 12.34;
        int doubleToEntero = (int)numeroDouble;

        System.out.println("De double a entero: " + doubleToEntero); // 12

        // de entero a double
        int entero2 = 987;
        double enteroToDouble = (double)entero2;

        System.out.println("El numero de entero a double es: " + enteroToDouble);
    }
}
```
## Constantes
```Java
public class Constantes {
    public static void main(String[] args) {
        // variables que no pueden cambiar su valor.
        final int currentlyAge = 45;
        System.out.println(currentlyAge); // 45
    }
}
```
## Operadores aritméticos
```Java
import java.util.Scanner;

public class Operadores_aritmeticos {
    public static void main(String[] args) {
        int valor1, valor2, resultado;

        // Ingreso de valores
        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese valor 1: ");
        valor1 = entrada.nextInt();

        System.out.println("Ingrese valor 2: ");
        valor2 = entrada.nextInt();

        // Suma
        resultado = valor1 + valor2;
        System.out.println("La suma es: " + resultado);

        // Resta
        resultado = valor1 - valor2;
        System.out.println("La resta es: "+ resultado);

        // Multiplicacion
        resultado = valor1 * valor2;
        System.out.println("La multiplicacion es: "+ resultado);

        // Division entera
        resultado = valor1 / valor2;
        System.out.println("La division sin parte decimal: "+ resultado);

        // Division con parte decimal
        float resultado2 = (float)valor1 / valor2;
        System.out.println("La division con parte decimal: "+ resultado2);

        // Residuo o Modulo
        resultado = valor1 % valor2;
        System.out.println("El residuo es: "+ resultado);
    }
}
```
## Operadores de incremento y decremento.
```Java
public class Incremento {
    public static void main(String[] args) {
        int valor1 = 5;
        System.out.println("Valor original: " + valor1); // 5

        // Incrementando el valor "posfijo"=> primero lee la variable y luego la incrementa.
        valor1++;
        System.out.println("Valor incrementado: " + valor1); // 6

        // Incrementando el valor "prefijo"=> primero la incrementa y luego la lee.
        ++valor1;
        System.out.println("Valor incrementado: " + valor1); // 7

        // Incrementar un numero especifico.
        valor1 +=5;
        System.out.println("El ultimo valor incrementado 5 unidades mas: " + valor1); // 12

        // Decremento
        int valor2 = 9;
        System.out.println("Valor original: " + valor2); // 9

        valor2--;
        System.out.println("Valor decrementado: " + valor2); // 8

        --valor2;
        System.out.println("Valor decrementado: " + valor2); // 7

        valor2 -=5;
        System.out.println("Valor final decrementado en 5 unidades: " + valor2); // 2

        // Incremento con la multiplicacion
        int valor3 = 10;
        System.out.println("valor original: " + valor3);

        // Incrementar por un factor de 2 veces.
        valor3 *=2;
        System.out.println("El valor incrementado por el producto es: " + valor3); // 20

        // Incrementar por un factor de division de 2 veces.
        valor3 /=5;
        System.out.println("El valor incrementado por el producto es: " + valor3); // 4
    }
}
```
## Operadores de comparación.
```Java
public class Operadores_comparacion {
    public static void main(String[] args) {
        int valor1 = 90, valor2 = 50;

        // Operador de igualdad (==)
        var resultado = valor1 == valor2; // false 90 no es igual a 50
        System.out.println(resultado);

        // Operador diferente(!=)
        var resultado2 = valor1 != valor2;
        System.out.println(resultado2); // true 90 es diferente a 50

        // Operador mayor que (> o >=)
        var resultado3 = valor1 > valor2;
        System.out.println(resultado3); // true 90 es mayor que 50

        // Operador menor que (< o <=)
        var resultado4 = valor1 <= valor2;
        System.out.println(resultado4); // false 90 no es menor que 50
    }
}
```
## Operadores lógicos.
```Java
public class Operadores_logicos {
    public static void main(String[] args) {

        boolean a = true, b = false;

        // Operador "and" &&
        var operadorAnd = a && b; // true and false
        System.out.println(operadorAnd); // false

        // Operador "or" ||
        var operadorOr = a || b; // true or false
        System.out.println(operadorOr); // true

        // Operador negacion "not" !
        var operadorNot = !b; // niega (false)
        System.out.println(operadorNot); // true

        // Operador XOR logico
        System.out.println(false ^ true); // solo necesita que una de las expresiones sea verdadera para que sea true
    }
}
```
## Condicionales If-else if-else.
```Java
import javax.swing.*;

public class Condicional_IF {
    public static void main(String[] args) {

        String nombre;
        int edad;

        nombre = JOptionPane.showInputDialog(null,"Ingresa tu nombre: ");
        String edadString = JOptionPane.showInputDialog(null,"Ingresa tu edad: ");
        edad = Integer.parseInt(edadString);

        // Analizando datos
        if(edad <= 12){
            JOptionPane.showMessageDialog(null,"Eres un niño(a).");
        }else if(edad > 12 && edad < 19){
            JOptionPane.showMessageDialog(null, "Eres adolescente.");
        }else{
            JOptionPane.showMessageDialog(null, "Eres un adulto.");
        }
    }
}
```
## Switch.
```Java
import java.util.Scanner;

public class Switch{
    public static void main(String[] args) {

        int DiaSemana;
        Scanner entrada = new Scanner(System.in);

        // ingreso de datos
        System.out.println("Ingrese el dia de la semana a consultar: ");
        DiaSemana = entrada.nextInt();

        switch(DiaSemana){
            case 1:
                System.out.println("Lunes");
                break;
            case 2:
                System.out.println("Martes");
                break;
            case 3:
                System.out.println("Miercoles");
                break;
            case 4:
                System.out.println("Jueves");
                break;
            case 5:
                System.out.println("Viernes");
                break;
            case 6:
                System.out.println("Sabado");
                break;
            case 7:
                System.out.println("Domingo");
                break;
            default:
                System.out.println("No encontrado.");
                break;
        }
    }
}
```
## Switch mejorado.
```Java
import java.util.Scanner;

public class Switch_mejorado {
    public static void main(String[] args) {
        int DiaSemana;
        Scanner entrada = new Scanner(System.in);

        // ingreso de datos
        System.out.println("Ingrese el dia de la semana a consultar: ");
        DiaSemana = entrada.nextInt();

        switch(DiaSemana){
            case 1 -> System.out.println("Lunes");
            case 2 -> System.out.println("Martes");
            case 3 -> System.out.println("Miercoles");
            case 4 -> System.out.println("Jueves");
            case 5 -> System.out.println("Viernes");
            case 6 -> System.out.println("Sabado");
            case 7 -> System.out.println("Domingo");
            default -> System.out.println("No encontrado.");
        }
    }
}
```
## Métodos con Strings.
```Java
import java.util.Scanner;

public class MetodoString {
    public static void main(String[] args) {
        String palabra1, palabra2;
        Scanner entrada = new Scanner(System.in);

        // ingreso de datos
        System.out.println("Ingrese primera palabra: ");
        palabra1 = entrada.next();

        System.out.println("Ingrese la segunda palabra: ");
        palabra2 = entrada.next();

        // NOTA: Solo funcionan con una sola palabra si es una oracion con espacios no funciona.
        // comparar textos => "equals"
        if (palabra1.equals(palabra2)){
            System.out.println("Las palabras son iguales");
        }else{
            System.out.println("No son iguales las palabras");
        }

        // comparar textos sin tomar en cuenta mayusculas => "equalsIgnoreCase"
        if (palabra1.equalsIgnoreCase(palabra2)){
            System.out.println("Las palabras son iguales, sin tomar en cuenta las mayusculas/minusculas!");
        }else{
            System.out.println("Las palabras no son iguales, sin tomar en cuenta las mayusculas/minusculas");
        }

        // comparar cantidad de caracteres => "compareTo" solo aplica a mismas minusculas o mismas mayusculas
        if((palabra1.compareTo(palabra2))==0){
            System.out.println("La palabra 1 tiene igual longitud de caracteres que la palabra 2!");
        }else{
            if((palabra1.compareTo(palabra2))>0){
                System.out.println("La palabra 1 tiene mas longitud de caracteres que la palabra 2!");
            }else{
                System.out.println("La palabra 2 tiene mas longitud de caracteres que la palabra 1!");
            }
        }
        // saber primer caracter de una palabra
        char caracter = palabra1.charAt(0);
        System.out.println("Primera letra de la palabra 1 es: " + caracter);

        // cantidad de caracteres de un texto
        System.out.println("La palabra 1 tiene " + palabra1.length() + " letras");
        System.out.println("La palabra 2 tiene " + palabra2.length() + " letras");

        // conocer caracteres especificos de un texto
        System.out.println(palabra1.substring(0,2)); // da los caracteres 0 y 1, no se incluye el 2.

        // conocer caracteres que esten en otra palabra
        int coincidencia = palabra1.indexOf(palabra2);
        if (coincidencia == -1){
            System.out.println(palabra1 + " no contiene: " + palabra2);
        }else{
            System.out.println(palabra1 + " contiene: " + palabra2);
        }

        // pasar texto a mayusculas
        System.out.println(palabra1 + " en mayusculas es " + palabra1.toUpperCase());

        // pasar texto a minusculas
        System.out.println(palabra2 + " en minusculas es " + palabra2.toLowerCase());
    }
}
```
## Método NextLine.
```Java
import java.util.Scanner;

public class Metodo_NextLine {
    public static void main(String[] args) {
        String texto1, texto2;
        Scanner entrada = new Scanner(System.in);

        System.out.println("Ingrese texto1: ");
        texto1 = entrada.nextLine();
        // texto1 = entrada.next(); // si se usa el metodo next no permite texto con espacios
        System.out.println("Ingrese texto2: ");
        texto2 = entrada.nextLine();

        System.out.println(texto1);
        System.out.println(texto2);
    }
}
```
## Bucle While.
```Java
import java.util.Scanner;

public class While {
    public static void main(String[] args) {
        
        int control = 0;

        // Bucle While
        while(control < 5){
            System.out.println(control);
            if(control == 3){
                System.out.println("Se ha encontrado el 3 en el bucle!");
                break; // rompe el bucle apenas encuentra el elemento 3
            }
            control ++;
        }
        
        // EJERCICIO DE PRACTICA TABLA DE MULTIPLICAR
        Scanner entrada = new Scanner(System.in);
        int valor;

        System.out.println("Ingrese el numero de la tabla a consultar: ");
        valor = entrada.nextInt();

        int contador = 1;
        System.out.println("Tabla del : " + valor);
        while(contador <= 10){
            System.out.println(valor + "x" + contador + "=" + valor * contador);
            contador++;
        }
        
        // EJERCICIO: control de login de usuario
        Scanner entrada = new Scanner(System.in);

        final String username = "hsimpson";
        final String password = "abc123";
        boolean acceso = false;

        while(!acceso){
            System.out.println("Ingrese su usuario: ");
            String usuario = entrada.next();

            System.out.println("Ingrese su clave: ");
            String clave = entrada.next();

            if (username.equals(usuario) && password.equals(clave)){
                System.out.println("User and password correct!");
                acceso = true;
            }else{
                System.out.println("Wrong user or password!");
            }
        }
    }
}
```
## Bucle Do-While.
```Java
import java.util.Scanner;

public class DO_WHILE {
    public static void main(String[] args) {
        int contador = 1;
        final var valor = 5;


//        // Bucle do - while
//        do {
//            System.out.println("Valor: " + ++contador);
//        }while(contador <= valor);

        Scanner entrada = new Scanner(System.in);

        int numero;
        do {
            System.out.println("Ingrese el numero 5!");
            numero = entrada.nextInt();
        }while (numero != 5);

    }
}
```
## Bucle For.
```Java
public class BUCLE_FOR {
    public static void main(String[] args) {
        // BUCLE FOR ASCENDENTE
        for (int f=0; f <= 3; f++){
            System.out.println("El valor es: " + f);
        }

        // BUCLE FOR DESCENDENTE
        for (int f=5; f >= 3; f--){
            System.out.println("El valor que desciende es: " + f);
        }

        // sumar pares dentro de rango de numeros
        int suma = 0;
        for (int i=0; i<=20; i++){
            if(i % 2 == 0){
                suma += i;
            }
        }
        System.out.println("La suma de todos lo numeros pares es: " + suma);
    }
}
```
## Break and continue.
```Java
public class BreakAndContinue {
    public static void main(String[] args) {
        int control, f = 0;

        // BREAK
        System.out.println("Cargando registros..");
        while(f <= 10){
            f++;
            if(f == 7){
                System.out.println("Registro " + f + " contiene error!\nSaliendo del sistema..");
                break;
            }
            System.out.println("Registro " + f + " cargado!");
        }

        // CONTINUE
        for(int i=0; i<=20; i++){
            if(i%2 == 0){
                continue;
            }
            System.out.println("Mostrando solo numeros impares " + i);
        }
    }
}
```
## Ejercicio con bucle while.
```Java
import javax.swing.*;

public class EJERCICIO_WHILE {
    public static void main(String[] args) {
        final String u_correcto = "Usuario01";
        final String p_correcto = "Abc123%";

        String username, password;
        int intentos = 1;
        final int max_intentos = 3;

        while(intentos <= max_intentos){
            username = JOptionPane.showInputDialog(null, "Ingrese su usuario: ");
            password = JOptionPane.showInputDialog(null, "Ingrese su contrasenia: ");

            if (u_correcto.equals(username) && p_correcto.equals(password)){
                JOptionPane.showMessageDialog(null, "Acceso correcto!" + "\n"
                                                                            + "Bienvenid@ " + u_correcto);
                break;
            }else{
                JOptionPane.showMessageDialog(null,"Usuario o clave incorrectos!"
                                            + "\nLe quedan " + (max_intentos-intentos) + " intentos restantes.");
            }
            if(intentos == 3){
                JOptionPane.showMessageDialog(null, "Se ha alcanzado los intentos maximos permitidos!");
            }
            intentos ++;

        }
    }
}
```
## Ejercicio con bucle for.
```Java
import javax.swing.*;

public class EJERCICIO_FOR {
    public static void main(String[] args) {
        boolean validar = false;

        for (int i = 0; !validar; i++) {
            String email = JOptionPane.showInputDialog(null, "Ingrese su email: ");

            if(email.contains("@") && email.endsWith(".com")){
                JOptionPane.showMessageDialog(null,"Email ingresado correctamente!");
                //validar = true;
                break;
            }else if(!email.contains("@") || !email.contains(".com")){
                JOptionPane.showMessageDialog(null, "Email no válido!");
            }

        }
    }
}
```
## Clase Math.
```Java
import java.util.Scanner;

public class ClaseMATH {
    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        // calculo de raiz cudrada
        System.out.println("Ingrese valor a calcular: ");
        int valor = entrada.nextInt();

        System.out.println("La raiz cuadrada de " + valor + " es: " + Math.sqrt(valor));

        // calculo de la potencia de un numero
        var base = 2;
        var potencia = 3;

        System.out.println("Potencia de 2 elevado a la 3: " + Math.pow(base,potencia));

        // valor absoluto
        var valor_absoluto = -2.5;
        System.out.println("El valor absoluto de "+ valor_absoluto + " es " + Math.abs(valor_absoluto));

        // mayor de 2 numeros
        var numero_1 = 499;
        var numero_2 = 435.5;

        System.out.println("El mayor valor entre " + numero_1 + " y " + numero_2 + " es " + Math.max(numero_1,numero_2));

        // menor valor entre 2 numeros
        System.out.println("El menor valor entre " + numero_1 + " y " + numero_2 + " es " + Math.min(numero_1,numero_2));

        // redondear un numero a entero mas cercano
        var numero_3 = 5.123;
        System.out.println("El numero " + numero_3 + " redondeado es " + Math.round(numero_3));

        // redondear un numero hacia abajo
        var numero_4 = 5.123;
        System.out.println("El numero " + numero_4 + " redondeado hacia abajo es " + Math.floor(numero_4));

        // redondear un numero hacia arriba a entero mas cercano
        var numero_5 = 5.123;
        System.out.println("El numero " + numero_5 + " redondeado hacia arriba es " + Math.ceil(numero_5));

        // numero aleatorio entre 0.0 y 1.0
        var aleatorio = Math.round(Math.random()*10);

        System.out.println("El valor aleatorio es: " + aleatorio);

        // funcion numero PI
        System.out.println("Numero PI: " + Math.PI);

        // seno de un angulo
        System.out.println("Seno de un angulo de 90: "+Math.sin(90));

        // coseno de un angulo
        System.out.println("Coseno de un angulo de 180: "+Math.cos(180));

        // logaritmo natural de un numero
        var log = 100;
        System.out.println("Logaritmo de: " + log + " = " + Math.log(log));

        // logaritmo base 10 de un numero
        var valor1 = 100;
        System.out.println("Logaritmo base 10 de: " + valor1 + " = " + Math.log10(valor1));

    }
}
```
## Arrays.
```Java
package Arrays;

import java.util.Arrays;

public class Arreglos {
    public static void main(String[] args) {
        // ARREGLO DE ENTEROS

        // declaracion de un array
        int[] numeros = new int[5];

        // inicializar un array FORMA 1
        numeros[0] = 101;
        numeros[1] = 32;
        numeros[2] = 53;
        numeros[3] = 48;
        numeros[4] = 105;

        // inicializar un array FORMA 2
        int[] numeros2 = {51,62,38,40,513};

        // consultar un elemento del array1
        System.out.println("Primer elemento del array: " + numeros[0]);

        // consultar un elemento del array2
        System.out.println("Primer elemento del array2: " + numeros2[0]);

        // ARREGLO DE CARACTERES
        String[] productos = new String[5];
        productos[0] = "manzanas";
        productos[1] = "uvas";
        productos[2] = "peras";
        productos[3] = "fresas";
        productos[4] = "kiwis";

        // consultar un elemento del array 'productos'
        System.out.println("Ultimo elemento del array de productos: " + productos[4]);

        // ordenando el array
        Arrays.sort(productos);

        // mostrar el array ordenado
        System.out.println(productos[0]);
        System.out.println(productos[1]);
        System.out.println(productos[2]);
        System.out.println(productos[3]);
        System.out.println(productos[4]);
    }
}
```
## Recorrer un array.
```Java
package Arrays;

import java.text.MessageFormat;

public class Arrays_recorrido {
    public static void main(String[] args) {

        String[] productos = {"martillo",
                            "destornillador",
                            "taladro",
                            "llave inglesa",
                            "pinzas"};
        
        // recorriendo el array con bucle FOR
        for (int f = 0; f < productos.length; f++) {
            String mensajefinal = MessageFormat.format("Producto {0}: {1}", f, productos[f]);
            System.out.println(mensajefinal);
        }
        System.out.println("-----------------------------");

        // recorriendo el array con bucle WHILE
        int counter = 0;
        while(counter < productos.length){
            String mensaje = String.format("Producto %d: %s", counter, productos[counter]);
            System.out.println(mensaje);
            counter++;
        }
    }
}
```
## Arrays paralelos.
```Java
package Arrays;

public class ArraysCombinados {
    public static void main(String[] args) {
        String[] productos = {"martillo",
                "destornillador",
                "taladro",
                "llave inglesa",
                "pinzas"};
        double[] precios = {12.50, 10.20, 200.00, 130.50, 20.35};

        for (int i = 0; i < productos.length; i++) {
            String mensaje = String.format("Producto %d: %s | precio: $%.2f",i+1, productos[i], precios[i]);
            System.out.println(mensaje);
        }

    }
}
```
## Operaciones con arrays.
```Java
package Arrays;

import java.text.MessageFormat;
import java.util.Scanner;

public class Arrays_Operaciones {
    public static void main(String[] args) {
        int[] ventas1 = {500,600,400,100,650};
        int[] ventas2 = {600,800,500,350,900};
        int[] total = new int[ventas1.length];

        // calculo de la suma de los 2 arrays
        System.out.println("Suma de valores: ");
        for (int i = 0; i < ventas1.length; i++) {
            int suma = ventas1[i] + ventas2[i];
            total[i] = suma;
        }

        // recorremos el array resultante
        for (int j = 0; j < total.length; j++) {
            System.out.println(total[j]);
        }

        // calculo de la suma de todo el array resultante
        int sumaTotal = 0;
        for (int k = 0; k < total.length; k++) {
            sumaTotal += total[k];
        }

        // mostramos el valor de la suma total del array
        System.out.println(String.format("La suma total es: %d",sumaTotal));

        // mayor valor de un array
        Scanner entrada = new Scanner(System.in);
        int[] numeros = new int[5];
        int mayor = 0;

        // llenando array
        for (int m = 0; m < 5; m++) {
            System.out.println(MessageFormat.format("Ingrese valor {0}: ", m+1));
            numeros[m] = entrada.nextInt();

            // analiza el valor mayor mediante comparaciones
            if (numeros[m] > mayor) {
                mayor = numeros[m];
            }

        }
        System.out.println(String.format("El valor mayor es: %d", mayor));

    }
}
```
## Métodos de los arrays.
```Java
package Arrays;

import java.util.Arrays;

public class Arrays_methos {
    public static void main(String[] args) {
        int[] numeros = {8,2,4,6,5,1,3,7};
        String[] letras = {"z","a","c","f","b","x"};

        // mostrar el array como cadena de texto
        System.out.println("Array original: " + Arrays.toString(numeros));
        System.out.println("Array original: " + Arrays.toString(letras));

        // organizar un array de enteros
        Arrays.sort(numeros);
        System.out.println("Array organizado: " + Arrays.toString(numeros));
        Arrays.sort(letras);
        System.out.println("Array organizado: " + Arrays.toString(letras));

        // comparar 2 arrays
        int[] numero1 = {1,2,3};
        int[] numero2 = {1,5,3};

        boolean iguales = Arrays.equals(numero1,numero2);
        System.out.println("Son iguales: " + iguales);

        // llenar un array
        int[] llenar = new int[5];
        Arrays.fill(llenar,1);

        System.out.println("Array llenado: " + Arrays.toString(llenar));

        // copiar un array
        int[] original = {1,2,3};
        int[] copia = Arrays.copyOf(original,5); // se crea un nuevo array de 5 elementos
        // con los elementos del array original

        System.out.println("Array copiado: " + Arrays.toString(copia));

    }
}
```
## Matrices.
```Java
package Arrays;

public class Matrices_40_41 {
    public static void main(String[] args) {
        int[][] numeros = new int[3][3];

        // llenado de la 1 fila de la matriz
        numeros[0][0] = 8;
        numeros[0][1] = 7;
        numeros[0][2] = 4;
        // llenado de la 2 fila de la matriz
        numeros[1][0] = 2;
        numeros[1][1] = 1;
        numeros[1][2] = 3;
        // llenado de la 3 fila de la matriz
        numeros[2][0] = 9;
        numeros[2][1] = 0;
        numeros[2][2] = 6;

        // [8 7 4]
        // [2 1 3]
        // [9 0 6]

        // recorrer la matriz con ciclo FOR por FILAS
        for (int i = 0; i < numeros.length; i++) {
            for (int j = 0; j < numeros.length; j++) {
                System.out.println(numeros[i][j]);
            }
        }

        System.out.println("---------------------");

        // otra forma de llenar una matriz
        int[][] matriz2 = {
                {3,4,1,2},
                {6,4,8,5},
                {9,8,0,9}
        };
        // recorrer la matriz con ciclo FOR por COLUMNAS
        for (int j = 0; j < matriz2[0].length; j++) {
            for (int i = 0; i < matriz2.length; i++) {
                System.out.println(matriz2[i][j]);
            }
        }

        System.out.println("-----------------------");

        // ver la matriz tal como se definio
        for (int i = 0; i < matriz2.length; i++) {
            for (int j = 0; j < matriz2[i].length; j++) {
                System.out.print(matriz2[i][j]);
            }
            System.out.println("");
        }
        System.out.println("----------------------------");
        // como calcular la longitud de las filas y columnas de una matriz bidimensional
        int[][] matriz3 = {
                {3,4,1,2,0},
                {6,4,8},
                {9,8,0,9,3},
                {1,5,3,7,1}
        };
        // cantidad de filas
        System.out.println("Cantidad de filas matriz: "+ matriz3.length); // 4

        // cantidad de columnas que posee la fila 0
        System.out.println("Cantidad de columnas matriz: " + matriz3[0].length); // 5

        // cantidad de columnas que posee la fila 1
        System.out.println("Cantidad de columnas matriz: " + matriz3[1].length); // 3
    }
}
```
## Programación orientada a objetos-POO.
```Java

```
##
```Java

```
##
```Java

```
##
```Java

```
##
```Java

```
##
```Java

```
##
```Java

```

