# Ej. 1 · Salida y GC: tu papel, tal cual

**2º simulacro** (25/10), ej. 1 del parcial 2025-1C, 1ª oportunidad. Nota: **95**.
Transcripción literal de la hoja. Lo tachado va ~~tachado~~ y lo que escribiste en rojo, en **negrita**.
Las correcciones están aparte, al final, para que no se mezclen con lo tuyo.

---

## 1.

### STACK

| Variable | Valores |
|---|---|
| `int X` | ~~?~~ ~~77~~ ~~74~~ ~~71~~ ~~68~~ ~~65~~ 62 |
| `int Y` | ~~?~~ ~~79~~ ~~150~~ ~~218~~ ~~283~~ 345 |
| `int Z` | ~~5~~ ~~79~~ ~~150~~ ~~218~~ 283 |
| `char W` | ~~'C'~~ 'N' |
| `int T` | ~~?~~ ~~77~~ ~~75~~ ~~73~~ ~~71~~ ~~69~~ 67 |
| `int[] A` | → (flecha azul al arreglo del heap) |
| `int[] B` | → (flecha verde al mismo arreglo) |

### HEAP

~~[0,0,0,0]~~ ~~[77,0,0,0]~~
~~[77,38,0,0]~~ ~~[77,38,154,0]~~
~~[67,38,154,0]~~ ~~[57,38,154,0]~~
~~[47,38,154,0]~~ ~~[37,38,154,0]~~
[27,38,154,0]

### Visión de los println:
1. 77-C-77-38
2. N-77-38-154

### Visión de los while:
1. 79-75-38-5
2. 150-73-38-79
3. 218-71-38-150
4. 283-69-38-218
5. 345-67-38-283

### GC

En el heap hay un solo arreglo de enteros **int[4]**, apuntado por A y B.
Además, cada **println** crea un **String** temporal con la concatenación.
Al menos son 7.
Al llegar al comentario final, sigue con referencias de A y B, por lo que el GC, no puede liberarlo.
Los **String** temporales no los apunta ninguna variable, cada uno queda elegible por el GC apenas terminan su **println**.
Cuando **main** termina, su frame sale del stack A y B, desaparecen y el arreglo queda elegible por el GC.
El GC no actúa sobre variables, sino sobre objetos del heap.
Por lo que el GC solo se ocupa de los arreglos y de los **string**.

---

## Correcciones (no están en el papel)

- **Z termina en 345, no en 283.** Después del último `println` todavía se ejecuta `Z = Y`. Al cerrar la traza, recorré la última vuelta del while **hasta la llave**.
- **Sumá una línea al GC:** «Los primitivos (X, Y, Z, T, W) viven en el frame de main, en el stack: no son objetos, el GC no los toca». Y si querés cerrar redondo: «elegible no es lo mismo que recolectado; el GC decide cuándo pasa».

## El código del ejercicio

```java
public static void main(String[] args) {
    int X, Y, Z = 5;
    char W;
    int T;
    int[] A = new int[4];
    int[] B = A;

    T = 77;
    W = 'C';
    X = T;
    A[0] = X;
    B[1] = A[0] / 2;

    System.out.println(X + "-" + W + "-" + B[0] + "-" + A[1]);

    W = (char) (T + 1);
    B[2] = A[0] * 2;

    System.out.println(W + "-" + T + "-" + B[1] + "-" + A[2]);

    while (A[0] > 30) {
        T -= 2;
        X -= 3;
        Y = X + Z;
        System.out.println(Y + "-" + T + "-" + B[1] + "-" + Z);
        Z = Y;
        A[0] -= 10;
    }

    // ¿Qué hace el garbage collector aquí? ¿Sobre qué variable?
}
```
