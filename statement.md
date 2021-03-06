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

Dato4: Recuerde que las cadenas de caracteres (strings) se comportan como arrays de tipo char, se puede utilizar el operador corchetes [] para acceder individualmente a las letras -> Ejemplo: string hh = "Hola"; hh[1] es la letra 'o'

Dato 5: Recuerde que un número está escrito en el sistema decimal donde cada cifra a la izquierda es 10 veces mayor que la siguiente
cifra a la derecha.

Ejemplo: '111' el primer '1' es 10 veces mayor que el segundo '1' y este es a su vez 10 veces mayor que el último 1. Es decir el número en
string '111' se puede convertir a un entero como la suma de 1 + 1x10 + 1x100

```C++ runnable
#include<iostream>
#include<string>

using namespace std;

int NumStringToInt(string numero)
{
	// Complete esta función siguiendo las recomendaciones anteriores
}

int main()
{
    string number1 = "45678945";
	cout<<NumStringToInt(number1)<<endl;
	string number2 = "-375907";
	cout<<NumStringToInt(number2)<<endl;
}
```

# ¿Cuál línea de código se ejecuta el mayor número de veces?

Analice la función testFunction y luego identifique cuál de sus líneas de código es la que se ejecuta el mayor número de veces cuando se corre el programa.

```C++ runnable
#include<iostream>

using namespace std;

int testFunction(int num1, int num2)
{
	int suma_pre = 0;
	
	while(num2 >= 0)
	{
	    int cuenta = 0;
	    
	    while(cuenta <= num2)
	    {
	        suma_pre += num1;
	        ++cuenta;
	    }
	    
	    --num2;
	}
	
	return suma_pre;
}

int main()
{
    int resultado = testFunction(3, 10);
    std::cout << "Resultado: " << resultado << std::endl;
}
```

# <i>InforMatic!</i>

Codifique en C++ la función inforMatic de modo que si el parámetro de entrada `num` es múltiplo de 3 se debe imprimir en pantalla: Infor. Si `num` es múltiplo de 5 se debe imprimir: Matic. Si `num` es múltiplo de 3 y 5 al mismo tiempo entonces debe se debe imprimir: InforMatic. En cualquier otro caso debe imprimir el valor de `num`.

Ejm: <ul><li>num = 6  -> Infor</li>
     <li>num = 15 -> InforMatic</li>
     <li>num = 20 -> Matic</li>
     <li>num = 8  -> 8</li></ul>

```C++ runnable
#include<iostream>

using namespace std;

void inforMatic(int num)
{
	// Complete esta función siguiendo las recomendaciones anteriores
}

int main()
{
    for(int i=0; i<21; ++i)
        inforMatic(i);
}
```

# Decodificador de permisos en Linux

Diseñe una función para decodificar secuencias de permisos en el sistema operativo Linux. La función recibe un string (cadena de caracteres) con los permisos que se le deben entregar a determinado archivo o aplicación (permisos de escritura: w, de lectura: r, de ejecución: x). Un permiso en linux se representa como un sting de 9 caracteres en el cual los 3 primeros caracteres corresponden a los permisos que tiene el usuario del equipo, los 3 caracteres siguientes a los permisos del grupo al cual pertenece el usuario y los 3 últimos a los permisos para cualquier otro usuario. 

Por ejemplo un permiso para que un archivo pueda ser leído o modificado por cualquier usuario del equipo sería así: `rw-rw-rw-`

Un permiso para que solo el usuario del equipo y los de su mismo grupo puedan ejecutar o "leer" cierto ejecutable sería así: `r-xr-x---`

El sistema operativo Linux prefiere que le envien los permisos codificados en un número de 3 cifras y no en un string de caracteres. Para esto es necesario convertir los caracteres al valor númerico que Linux "entiende". El sistema de conversión es el siguiente:

<ul><li>r : 4</li>
<li>w : 2</li>
<li>x : 1</li>
<li>- : 0</li></ul>

Cada subconjunto de 3 caracteres contiguos (es decir, los permisos para usuario, grupo y otros) se convierte a sus valores numéricos y se suman para obtener un único digito para representar los permisos de ese usuario. Ejemplo: El permiso de archivo que vimos anteriormente `rw-rw-rw-` se debe codificar como 666, y el permiso de la aplicación `r-xr-x---` se codifica como 550.

La función decodePermits recibe como parametro de entrada un string que representa los permisos en caracteres y debe retornar un número entero con los permisos decodificados en su representación numérica.

```C++ runnable
#include<iostream>
#include<string>

using namespace std;

int decodePermits(const string& permits)
{
	// Complete esta función siguiendo las recomendaciones anteriores
}

int main()
{
    string permit1 = "rw-r--r--";
    string permit2 = "rwxr-x--x";
    string allpermits = "rwxrwxrwx";
    
    std::cout << decodePermits(permit1) << std::endl;
    std::cout << decodePermits(permit2) << std::endl;
    std::cout << decodePermits(allpermits) << std::endl;
    
    return 0;
}
```


# Aplicaciones de la programación

Desarrolle una aplicacion de cifrado sencillo para una trama de datos de tipo entero.
La trama de datos es simplemente un arreglo de enteros de 20 posiciones.
Una vez incializada la trama, esta debe pasarse a una funcion que la debe cifrar siguiendo el procedimiento 
que se describe a continuacion:

1. La funcion de cifrado ademas de la trama recibe otro parametro que indica cuantas veces se debe ejecutar el 
proceso de cifrado en la trama (rondas de actualización).

2. El proceso de cifrado consiste simplemente en actualizar cada posicion de la trama de la siguiente manera:
	a. Cada posicion par se actualiza con el valor obtenido de la resta de los valores de las 2 posiciones
       vecinas (izquierda - derecha).
    b. Cada posicion impar se actualiza con el valor obtenido de la suma de los valores de las 2 posiciones
       vecinas (izquierda + derecha).	   

3. Es importante mencionar que las posiciones se actualizan con los ultimos valores de la trama, es decir, una posicion
   no debe actualizarse con los valores recien actualizados de sus vecinos sino con los valores previos de la ultima
   ronda de actualizacion.
   
4. Al final de las n rondas de cifrado la trama queda completamente cifrada.

5. Las posiciones de los extremos (0 y 19) se actualizan asumiendo que el vecino faltante es:
   Para el caso de la posicion 0 el vecino a izquierda sera la posicion 19.
   Para el caso de la posicion 19 el vecino a derecha sera la posicion 0.
   
6. La funcion de cifrado debe nombrarse cifraData y puede tener o no valor de retorno, eso depende de la forma en que
   el estudiante la desarrolle.
   
7. Un porcentaje de la calificacion corresponde a la interpretacion del ejercicio. Usted como ingeniero debe leer bien los
   pasos descritos hasta este punto y luego plantear la solucion mas conveniente para el ejercicio.

8. En la funcion main se debe imprimir en pantalla la trama completa antes del cifrado y luego del proceso de cifrado.
  
Ejemplo:

Trama: {1,45,92,216,28,63}

Numero de rondas de actualizacion: 3

Trama cifrada que se obtiene:

	Ronda 1: {18,93,-171,120,153,29}
	
	Ronda 2: {-64,-153,-27,-18,91,171}
	
	Ronda 3: {324,-91,-135,64,-189,27}  Esta es la trama final cifrada

```C++ runnable
#include <iostream>

using namespace std;

void cifraData(int arr[], int rondas)
{
    // Complete esta función siguiendo las recomendaciones anteriores
}

int main()
{
    int trama[6]={1,45,92,216,28,63}; //Trama de ejemplo
    cifraData(trama, 3); // Llamado de ejemplo
    
    return 0;
}

```

