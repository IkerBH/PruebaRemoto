# Tema 1

- uno
- dos
- tres

```java

import java.util.Scanner;

// Definición de la clase CuentaBancaria
class CuentaBancaria {
    // Atributos (propiedades del objeto)
    private String titular;
    private double saldo;

    // Constructor: Inicializa el objeto cuando se crea
    public CuentaBancaria(String titular, double saldoInicial) {
        this.titular = titular;
        this.saldo = saldoInicial;
    }

    // Método para depositar dinero
    public void depositar(double cantidad) {
        if (cantidad > 0) {
            saldo += cantidad;
            System.out.println("✅ Depósito exitoso de $" + cantidad);
        }
    }

    // Método para retirar dinero con validación
    public void retirar(double cantidad) {
        if (cantidad > 0 && cantidad <= saldo) {
            saldo -= cantidad;
            System.out.println("✅ Retiro exitoso de $" + cantidad);
        } else {
            System.out.println("❌ Error: Fondos insuficientes o cantidad inválida.");
        }
    }

    // Método para mostrar el estado de la cuenta
    public void mostrarInformacion() {
        System.out.println("\n--- Estado de la Cuenta ---");
        System.out.println("Titular: " + titular);
        System.out.println("Saldo actual: $" + saldo);
        System.out.println("---------------------------\n");
    }
}

// Clase principal que ejecuta el programa
public class Main {
    public static void main(String[] args) {
        // Creación de un objeto de la clase CuentaBancaria
        CuentaBancaria miCuenta = new CuentaBancaria("Ana López", 500.0);

        // Mostramos el saldo inicial
        miCuenta.mostrarInformacion();

        // Realizamos operaciones
        miCuenta.depositar(200.50);
        miCuenta.retirar(100.0);
        
        // Intentamos retirar más de lo que hay
        miCuenta.retirar(800.0);

        // Mostramos el saldo final
        miCuenta.mostrarInformacion();
    }
}


```

#Tema 2

Nacher despiereta
