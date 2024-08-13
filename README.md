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
