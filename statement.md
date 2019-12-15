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

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced C++ template](https://tech.io/select-repo/598)
