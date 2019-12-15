# Fkujo de ejecución de aplicaciones en C++

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

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced C++ template](https://tech.io/select-repo/598)
