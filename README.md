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
