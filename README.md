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
