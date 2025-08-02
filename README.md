# USO DE IF - ELSE En C++ 

En programación informática, utilizamos la if - else para ejecutar un bloque de código bajo ciertas condiciones y otro bloque de código bajo diferentes condiciones.

## IF, Si entonces 

```c++
if (condition) {
  // cuerpo de la instrucción if
}
```


La **if** declaración evalúa la condición dentro de los paréntesis ( ).

    - Si la condición evalúa a if averdadero, se ejecuta el código dentro del cuerpo.
    - Si la condición evalúa a if FALSO, se omite el código dentro del cuerpo.

```c++
// Programa imprime un numero entero
// Si el usuario ingresa un numero entero negativo no se mostrara lo que esta dentro del bloque

#include <iostream>
using namespace std;

int main() {

  int number;

  cout << "Ingrese un entero: ";
  cin >> number;

  // Verifica si el numero es positivo
  if (number > 0) {
    cout << "Ingresaste un numero positivo: " << number << endl;
  }

  cout << "Esta instrucción siempre se ejecuta.";

  return 0;
}
```

## ELSE, Si de lo contrario 

La declaración *if* puede tener una cláusula opcional *else*.

```c++
if (condition) {
  // bloque de código si la condición es verdadera
}
else {
  // bloque de código si la condición es falsa
}
```


Si la condición evalúa **VERDADERO**,

    1. if Se ejecuta el código dentro del cuerpo
    2. El código dentro del cuerpo else se omite de la ejecución

Si la condición evalúa **FALSO**,

    1. elseSe ejecuta el código dentro del cuerpo de
    2. El código dentro del cuerpo if se omite de la ejecución

```c++
//Programa para comprobar si un número entero es positivo o negativo
// Este programa considera el 0 como un número positivo
#include <iostream>
using namespace std;

int main() {

  int number;

  cout << "Ingrese un entero: ";
  cin >> number;

  if (number >= 0) {
    cout << "Ingresaste un numero entero: " << number << endl;
  }
  else {
    cout << "Ingresaste un numero entero negativo: " << number << endl;
  }

  cout << "Esta linea siempre se imprime.";

  return 0;
}
```


# Declaración switch

La declaración **SWITCH** nos permite ejecutar un bloque de código entre muchas alternativas.

Puedes hacer lo mismo con la instrucción if - else . Sin embargo, la sintaxis de la instrucción switch es mucho más fácil de leer y escribir.

```c++
switch (expression)  {
    case constant1:
        // código que se ejecutará si
        // La expresión es igual a la constante 1;
        break;

    case constant2:
        // código que se ejecutará si
        // La expresión es igual a la constante 2;
        break;
        .
        .
        .
    default:
        // código que se ejecutará si
        // La expresión no coincide con ninguna constante.
}
```

## ¿Cómo funciona la sentencia switch?

La expresión`evalúa una vez y se compara con los valores de cada etiqueta case etiqueta.

-   Si hay una coincidencia, se ejecuta el código correspondiente después de la etiqueta coincidente. Por ejemplo, si el valor de la variable es igual a , se ejecuta  el código posterior hasta que se encuentra la instrucción break
-   Si no hay coincidencia, se ejecuta el código siguiente default.

```c++
// Program to build a simple calculator using switch Statement
#include <iostream>
using namespace std;

int main() {
    char oper;
    float num1, num2;
    cout << "Introduzca un operador (+, -, *, /): ";
    cin >> oper;
    cout << "Introduzca dos números: " << endl;
    cin >> num1 >> num2;

    switch (oper) {
        case '+':
            cout << num1 << " + " << num2 << " = " << num1 + num2;
            break;
        case '-':
            cout << num1 << " - " << num2 << " = " << num1 - num2;
            break;
        case '*':
            cout << num1 << " * " << num2 << " = " << num1 * num2;
            break;
        case '/':
            cout << num1 << " / " << num2 << " = " << num1 / num2;
            break;
        default:
            // operator is doesn't match any case constant (+, -, *, /)
            cout << "¡Error! El operador no es correcto.";
            break;
    }

    return 0;
}
```

**Cómo funciona este programa**

-  Primero solicitamos al usuario que ingrese el operador deseado . Esta entrada se almacena en la char variable denominada oper.
-  Luego solicitamos al usuario que ingrese dos números, que se almacenan en las variables flotantes. número 1 y número 2.
-  Luego, la switch declaración se utiliza para verificar el operador ingresado por el usuario:
    1.  Si el usuario ingresa `+`, se realiza la suma de los números.
    2.  Si el usuario ingresa `-`, se realiza una resta sobre los números.
    3.  Si el usuario ingresa `*`, se realiza la multiplicación de los números.
    4.  Si el usuario ingresa `/`, se realiza la división de los números.
    5.  Si el usuario ingresa cualquier otro carácter, se imprime el código predeterminado.

***

**Pagina donde se realizo la investigación:** [PROGRAMIZ](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://translate.google.com/translate%3Fu%3Dhttps://www.programiz.com/cpp-programming/if-else%26hl%3Des%26sl%3Den%26tl%3Des%26client%3Dsrp&ved=2ahUKEwi-qpTI7-mOAxXJRTABHUqdOp8QFnoECBgQAQ&usg=AOvVaw2iWpO-J2znRru3xjDP3u7u)

