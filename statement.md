# Flujo de ejecución de aplicaciones en C++

A continuación hay 3 cortos programas en C++. Su tarea es explicar en comentarios hechos en el mismo código el porque del resultado final de la ejecución y que es lo que sucede en cada una de las líneas de código para llegar a ese resultado en específico. Es decir, en los comentarios se debe explicar como va cambiando el valor de las variables, el resultado de operaciones aritméticas, lógicas o condicionales, el número de iteraciones de los ciclos, entre otros.

```C++ runnable
// Codigo número 1
#include <iostream>

using namespace std;

int main() 
{
    int i = 10;
    float a = 1000.0;
    
    while(i > 0)
    {
        i /= 2;
        a /= 10;
    }
    
    cout<<"El valor final de la variable 'a' es: "<<a<<endl;
    return 0;
}
```

```C++ runnable
// Codigo número 2
#include <iostream>

using namespace std;

int main() 
{
    int i = 1, j = 2;
    
    if(i > j && j > i)
        i++;
    if(i > j || j > i)
        j++;
    if(i | j)
        i++;
    if(i & j)
        j++;
    
    cout<<i * j<<endl;
    return 0;
}
```

```C++ runnable
// Codigo número 3
#include <iostream>

using namespace std;

int main() 
{
    for(int i = 0; i < 4; ++i)
    {
        switch(i)
        {
            case 0: cout<<"0";
            case 1: cout<<"1"; continue;
            case 2: cout<<"2"; break;
            default: cout<<"D"; break;
        }
        
        cout<<"*";
    }
    return 0;
}
```

# Composición de funciones y recursión

La composición de funciones es una característica esencial de la programación estructurada o procedimental, y se refiere simplemente al hecho de que una función se puede definir como una composición de distintas invocaciones a otras funciones o incluso de invocaciones a sí misma. A esto último que se ha mencionado se le conoce como recursión, y es la capacidad que tienen las funciones de invocarse a sí mismas. El código a continuación permite calcular el máximo común divisor entre los elementos que componen un arreglo de números enteros

```C++ runnable
#include <iostream> 
using namespace std; 

// Función que retorna el MCD entre dos números a y b
int mcd(int a, int b) 
{ 

    //Desarrolle esta función de acuero al siguiente algoritmo:
    // Si el valor del número 'a' es igual a cero entonces retorne el valor de 'b'
    // Si 'a' no es cero, entonces retorne el resultado de ejecutar mcd (recursión)
    // pero los parámetros de entrada son primero: el módulo entre 'b' y 'a', y segundo el número 'a'
} 

// Función para encontrar el MCD de un arreglo de números
int mcdArreglo(int arr[], int n) 
{ 
    //Declare una variable 'resultado' e inicialicela con el primer elemento del arreglo 'arr'
    //Calcule el MCD para los 'n' números del arreglo: en la variable 'resultado' almacene el 
    //retorno de ejecutar la función mcd entre el elemento 'i' del arreglo y el valor actual de 
    //la variable 'resultado'. Recuerde que su ciclo debe ir desde la segunda posición del arreglo
    //hasta el último elemento del arreglo.
    //Finalmente retorne la variable 'resultado'
} 

// Ejecución de la aplicación (No modifique esta función!)
int main() 
{ 
	int arr[] = { 2, 4, 6, 8, 16 }; 
	int n = sizeof(arr) / sizeof(arr[0]); //Calcula el tamaño del arreglo (número de elementos)
	cout << mcdArreglo(arr, n) << endl; 
	return 0; 
} 
```

# Conversión entre distintos tipos de datos

La función NumSringToInt es una función que debe convertir un número escrito en letras (cadena de caracteres) 
en un número de tipo entero (int), usted debe agregar las líneas de código necesarias para implementar dicha funcionalidad.
Se debe garantizar que se convierten números enteros positivos y negativos.
Se debe garantizar que la función no intente convertir un número que sobrepasa la capacidad del tipo de dato int.
Utilice el tipo de dato "string" en caso de necesitar alguna variable para almacenar cadenas de caracteres.
Dato1: La representación en caracter (ASCII) de un número natural (0 al 9) es igual al número + 48 (o bien 0x30 en hexa)
Ejemplo: '9' = 9 + 48 = 0x09 + 0x30
Dato2: Para verificar la longitud de la cadena de caracteres que representa un número puede usar el operador size()
Ejemplo: string numero = "123456" -> numero.size() da como resultado 6
Dato3: Solo puede utilizar declaración de variables, operadores de C++ y estructuras de control para codificar la solución.
Dato4: Recuerde que las cadenas de caracteres (strings) se comportan como arrays de tipo char, se puede utilizar el operador
corchetes [] para acceder individualmente a las letras -> Ejemplo: string hh = "Hola"; hh[1] es la letra 'o'
Dato 5: Recuerde que un número está escrito en el sistema decimal donde cada cifra a la izquierda es 10 veces mayor que la siguiente
cifra a la derecha.
Ejemplo: '111' el primer '1' es 10 veces mayor que el segundo '1' y este es a su vez 10 veces mayor que el último 1. Es decir el número en
string '111' se puede convertir a un entero como la suma de 1 + 1*10 + 1*100

```C++ runnable
#include<iostream>
#include<string>

using namespace std;

int NumStringToInt(string numero)
{
	
	
}

int main()
{
    string number = "45678945";
	cout<<NumStringToInt(number)<<endl;
	string number = "-375907";
	cout<<NumStringToInt(number)<<endl;
}

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced C++ template](https://tech.io/select-repo/598)
