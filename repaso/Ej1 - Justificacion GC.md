# Ej. 1 · Salida y GC: tu respuesta en papel

Simulacro armado del **25/10** (ej. 1 del parcial 2025-1C, 1ª oportunidad). Nota: **95**.
Es tu respuesta **tal cual la escribiste en papel**, pasada a texto ese mismo día. Lo único marcado es la corrección.
El código está en `teoria/cb100/app/src/main/java/ar/uba/fi/cb100/practica/ej1_gc/TrazaParcial2025.java`.

---

## Salida

**Salida de los println:**
1. `77-C-77-38`
2. `N-77-38-154`

**Salida del while:**
1. `79-75-38-5`
2. `150-73-38-79`
3. `218-71-38-150`
4. `283-69-38-218`
5. `345-67-38-283`

## Estado al final

X = 62, Y = 345, Z = 345, T = 67, W = 'N', A y B apuntan al mismo arreglo [27, 38, 154, 0].

> **CORREGIDO:** en el papel, Z quedó en 283. Termina en **345** porque después del último `println` se ejecuta `Z = Y`.

## GC

En el heap hay un solo arreglo de enteros int[4], apuntado por A y B.
Además, cada println crea un String temporal con la concatenación. Al menos son 7.
Al llegar al comentario final, sigue con referencias de A y B, por lo que el GC no puede liberarlo.
Los String temporales no los apunta ninguna variable: cada uno queda elegible por el GC apenas termina su println.
Cuando main termina, su frame sale del stack (A y B desaparecen) y el arreglo queda elegible por el GC.
El GC no actúa sobre variables, sino sobre objetos del heap: los primitivos (X, Y, Z, T, W) viven en el stack.
Por lo que el GC solo se encarga de los arreglos y de los String.

---

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

## Para el parcial: la misma justificación, en 5 puntos

1. **Objetos del heap:** cuántos hay y qué variables los apuntan (`B = A` copia la referencia, no el arreglo).
2. **Strings temporales:** cada `println` con `+` crea String nuevos; nadie los apunta, quedan elegibles al terminar el `println`.
3. **En el comentario:** lo que sigue referenciado no se libera; queda elegible cuando termina `main` y su frame sale del stack.
4. **Primitivos:** viven en el frame del stack; no son objetos, el GC no los toca.
5. **Sobre qué actúa:** sobre objetos, no sobre variables. Elegible no es lo mismo que recolectado.

Y al cerrar la traza: recorré la última vuelta del while **hasta la llave**.
