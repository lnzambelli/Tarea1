package main;

import javafx.util.converter.IntegerStringConverter;

import java.lang.*;
import java.util.Scanner;

public class Start {
    public static void main(String[] args) {
        //LecturaPorTeclado();
        System.out.println ("Ingrese valor de frecuencia cardiaca");
        int valor = LecturaPorTeclado();
        Ejercicio1(valor);
        Ejercicio2();
    }

    public static Integer LecturaPorTeclado() {;
        Scanner scanner = new Scanner(System.in);
        int capturedText = scanner.nextInt();

        System.out.println("El valor ingresado es: " + capturedText);
        return capturedText;
    }

    public static void Ejercicio1(int valor) {
        if (valor < 60){
            System.out.println ("BRADICARDIA");
        }else{
            System.out.println ("TAQUICARDIA");
        }

    }
    public static void Ejercicio2() {
        int compresiones = 1;
        int insufraccion = 1;
        while (compresiones<=100){
            System.out.println ("Realizando compresion N° "+compresiones);
            if (compresiones%30==0){
                for (int i=1;i<=2;i++){
                    System.out.println ("Realizando insufraccion N° "+insufraccion);
                    insufraccion++;
                }
            }
            compresiones++;
        }
    }
}