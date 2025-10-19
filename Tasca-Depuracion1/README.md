# UD1 - Ejercicios de Java

## 1. Qué hacen estas dos líneas de código
```java
string2 = string2.substring(0, string2.length() - 1);
string2 = string2 + "1";
```
**Respuesta:** Estas dos líneas modifican `string2` quitando su último carácter y añadiendo `"1"` al final.

---

## 2. Por qué no funciona `==` para comparar Strings
```java
if (string1 == string2) { ... }
```
**Respuesta:** En Java, `==` comprueba si las variables apuntan al mismo objeto, no si su contenido es igual. Por eso no funciona para comparar Strings por valor.

---

## 3. Cómo solucionarlo
```java
if (string1.equals(string2)) { ... }
```
**Respuesta:** Para solucionarlo debemos sustituir `if (string1 == string2)` por `if (string1.equals(string2))`.

---

## 4. Qué valen las variables antes del `if`
**Respuesta:**  
`string1 = "string1"` y `string2 = "string1"`

---

## 5. Código corregido
```java
if (string1.equals(string2)) {
    System.out.println("SON IGUALES " + a);
} else {
    System.out.println("SON DIFERENTES");
}
```

---

## 6. Por qué la función no funciona desde `main`
**Respuesta:**  
- `main` es `static` y pertenece a la clase.  
- `funcion2` no es `static` y pertenece a un objeto.  
- Por eso no es posible llamarlo directamente desde `main`.

---

## 7. Cómo solucionarlo
**Respuesta:** Hay dos soluciones:  

1. Hacer la función `static`:
```java
public static void funcion2() { ... }
```

2. Crear un objeto de la clase y llamar a la función desde él:
```java
ED_Debug obj = new ED_Debug();
obj.funcion2();
```

**Resumen:** Los métodos `static` se pueden llamar directamente desde `main`, mientras que los métodos no `static` requieren un objeto para ser llamados.

