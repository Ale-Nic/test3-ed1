# test3-ed1

## Examen Tipo Test: Estructuras de Datos I

**Pregunta 1 ¿Qué hace mal la siguiente función al intentar insertar un nodo al principio de una lista?**
```cpp
void insertarInicio(TNodo_Lista* elementos, float valor) {
  TNodo_Lista* nuevo = new TNodo_Lista;
  nuevo->Datos = valor;
  nuevo->Siguiente = elementos;
  elementos = nuevo;
}
```
A) Inserta correctamente el nodo.  
B) Produce fuga de memoria.  
C) No actualiza correctamente el puntero original.  
D) El puntero Siguiente apunta a NULL.  

**Pregunta 2 ¿Cuál es la forma correcta de crear dinámicamente una tabla de 100 elementos tipo int?**  
A) int tabla[100];  
B) int* tabla = malloc(100);  
C) int* tabla = new int[100];  
D) int* tabla = new int(100);  

**Pregunta 3 ¿Qué opción describe mejor la ventaja de una lista implementada con nodos enlazados frente a una con tabla dinámica?**  
A) Menor uso de memoria.  
B) Acceso directo más rápido.  
C) Permite inserciones y borrados sin necesidad de mover elementos.  
D) Facilita el recorrido hacia atrás.  

**Pregunta 4 Dado el siguiente fragmento de código, ¿qué operación se está realizando?**
```cpp
colaPersonas.seekg(sizeof(Persona)*4, ios::beg);
colaPersonas.read((char*)&p, sizeof(Persona));
```
A) Lectura secuencial del 5º elemento de la cola.  
B) Lectura del primer elemento de la cola.  
C) Lectura directa del 5º elemento del archivo.  
D) Escritura directa en el archivo.  

**Pregunta 5 ¿Qué ocurre si se realiza una escritura con write() en un archivo binario en una posición ya ocupada?**
A) Se inserta un nuevo bloque.  
B) Se borra todo el archivo.  
C) Se sobrescribe la información existente.  
D) Se produce un error de compilación.  

**Pregunta 6 ¿Cuál es el error conceptual en el siguiente código?**
```cpp
void borrarLista(TNodo_Lista* elementos) {
  TNodo_Lista* sig;
  while (elementos != NULL) {
    sig = elementos->Siguiente;
    delete elementos;
    elementos = sig;
  }
}
```
A) No libera correctamente los nodos.  
B) Accede a memoria no reservada.  
C) El puntero original queda colgando.  
D) Borra dos veces el mismo nodo.  

**Pregunta 7 ¿Qué tipo de acceso proporciona el siguiente código?**
```cpp
archivo.seekg(0, ios::end);
int tam = archivo.tellg();
```
A) Acceso secuencial al final del archivo.  
B) Acceso aleatorio para lectura.  
C) Escritura secuencial.  
D) Consulta del tamaño del archivo.  

**Pregunta 8 ¿Cuál de las siguientes sentencias de C++ crea correctamente un objeto cliente dinámico con constructor por defecto?**  
A) cliente obj;  
B) cliente* obj = cliente();  
C) cliente* obj = new cliente;  
D) cliente obj = new cliente();  

**Pregunta 9 ¿Cuál es el propósito de la clase ifstream en C++?**  
A) Escribir datos en archivos de texto.  
B) Leer datos de archivos.  
C) Eliminar archivos temporales.  
D) Acceder a archivos binarios en modo escritura.  

**Pregunta 10 ¿Qué operación realiza la siguiente función?**
```cpp
void modificar(int i, float e) {
  TNodo_Lista* nodo = Anterior(i);
  if (nodo == NULL)
    elementos->Datos = e;
  else
    nodo->Siguiente->Datos = e;
}
```
A) Inserta un nuevo nodo en la posición i.  
B) Modifica el valor del nodo en la posición i.  
C) Recorre la lista hasta el final.  
D) Elimina el nodo de la posición i.  

**Pregunta 11 ¿Qué hace el operador -> en el siguiente código?**
```cpp
cliente* c = new cliente;
c->dni = 12345678;
```
A) Asigna un puntero a otro.  
B) Apunta al método de la clase.  
C) Accede a un campo de la clase mediante puntero.  
D) Declara una clase.  

**Pregunta 12 En una pila implementada con nodos enlazados, ¿dónde se encuentra el tope de la pila?**  
A) En el nodo final de la lista.  
B) Siempre en el primer nodo.  
C) En el nodo con menor dirección.  
D) En el puntero a NULL.  

**Pregunta 13 ¿Qué ocurre si no se libera memoria reservada dinámicamente con new?**  
A) El sistema la recupera automáticamente.  
B) Se borra al finalizar el programa.  
C) Se produce una fuga de memoria.  
D) Se provoca un error de compilación.  

**Pregunta 14 ¿Qué ventaja ofrece el uso de plantillas en C++?**  
A) Permite herencia múltiple.  
B) Reduce el número de clases necesarias.  
C) Permite escribir código genérico para múltiples tipos.  
D) Evita el uso de punteros.  

**Pregunta 15 ¿Cuál es el propósito del método Anterior(i) en las listas implementadas dinámicamente?**  
A) Eliminar el nodo anterior.  
B) Insertar un nodo al principio.  
C) Encontrar el nodo anterior al nodo en la posición i.  
D) Contar los nodos desde el inicio.  

**Pregunta 16 ¿Qué ocurre si se intenta acceder a un archivo con ifstream que no existe?**  
A) Se crea el archivo vacío.  
B) Se abre en modo escritura.  
C) Se produce un error lógico detectable con .fail().  
D) Se lanza una excepción.  

**Pregunta 17 ¿Qué error comete el siguiente código?**
```cpp
template <class T>
void mostrar(T dato) {
  cout << dato << endl;
}
mostrar<int>();
```
A) No se puede invocar sin argumento.  
B) No se puede usar template con tipos primitivos.  
C) cout no acepta plantillas.  
D) No hay error.  

**Pregunta 18 ¿Cuál es la diferencia principal entre una lista simplemente enlazada y una doblemente enlazada?**  
A) La segunda permite nodos de distinto tipo.  
B) La segunda permite recorrer la lista en ambos sentidos.  
C) La primera requiere más memoria.  
D) La primera permite inserciones al final.  

**Pregunta 19 ¿Cuál es el motivo de error en esta función?**
```cpp
void insertar(TNodo* Lista, int valor) {
  TNodo* nuevo = new TNodo;
  nuevo->Datos = valor;
  nuevo->Siguiente = Lista;
  Lista = nuevo;
}
```
A) Lista debería pasarse por puntero a puntero.  
B) nuevo no se inicializa correctamente.  
C) valor es un parámetro no válido.  
D) Siguiente apunta a NULL.  

**Pregunta 20 ¿Qué tipo de estructura describe una cola?**  
A) LIFO.  
B) FILO.  
C) Árbol binario.  
D) Puntero circular.  



**Pregunta 21 ¿Qué ocurre si se ejecuta este fragmento sin comprobar si new ha devuelto NULL?**
```cpp
TNodo_Lista* nodo = new TNodo_Lista;
nodo->Datos = 5.0;
```
A) Siempre se ejecuta correctamente.  
B) Se produce una excepción automáticamente.  
C) Puede causar acceso a memoria inválida si new falla.  
D) El compilador impide compilarlo sin verificación.  

**Pregunta 22 En el TAD Cola implementado con tabla circular, ¿qué ocurre cuando fin == inicio?**  
A) La cola está llena.  
B) La cola está vacía.  
C) Puede estar llena o vacía, depende del contador.  
D) Hay un error lógico.  

**Pregunta 23 ¿Qué ventaja presenta el uso de template<class T> en la implementación del TAD Lista?**  
A) Aumenta la velocidad de ejecución.  
B) Permite definir múltiples funciones simultáneamente.  
C) Evita tener que duplicar código para distintos tipos de datos.  
D) Genera código más legible.  

**Pregunta 24 ¿Qué hace el siguiente método en una clase de lista genérica?**
```cpp
bool esvacia() {
  return (n == 0);
}
```
A) Inserta un elemento en la lista vacía.  
B) Verifica si la lista está vacía.  
C) Inicializa la lista.  
D) Elimina todos los elementos.  

**Pregunta 25 ¿Qué característica tiene un archivo abierto con las opciones ios::app | ios::binary?**  
A) Se borra su contenido al abrirlo.  
B) Se escribe al principio del archivo.  
C) Solo se puede leer en modo texto.  
D) Se añade contenido al final sin modificar el anterior.  

**Pregunta 26 ¿Cuál de los siguientes errores es típico al usar delete sobre memoria no reservada con new?**  
A) Error de compilación.  
B) Excepción de tipo std::invalid_argument.  
C) Comportamiento indefinido.  
D) No ocurre nada.  

**Pregunta 27 ¿Qué hace este código en contexto de una cola con acceso directo?**
```cpp
cola.seekp(sizeof(Persona)*i, ios::beg);
cola.write((char*)&p, sizeof(Persona));
```
A) Inserta el elemento p al final de la cola.  
B) Sobrescribe el elemento en la posición i.  
C) Inserta un nuevo elemento al inicio.  
D) Añade un elemento vacío.  

**Pregunta 28 ¿Qué error comete esta plantilla sobrecargada?**
```cpp
template <class T>
T maximo(T a, T b) {
  return (a > b) ? a : b;
}

char* maximo(char* a, char* b) {
  return (strcmp(a, b) > 0) ? a : b;
}
```
A) No se puede sobrecargar una plantilla.  
B) La especialización debería usar template<>.  
C) El compilador no sabrá cuál usar.  
D) No hay error.  

**Pregunta 29 ¿Cuándo es útil usar typename en lugar de class en plantillas?**  
A) Cuando se trabaja solo con tipos básicos.  
B) Cuando el parámetro es un puntero.  
C) Son equivalentes en plantillas.  
D) typename solo funciona con structs.  

**Pregunta 30 ¿Cuál es el objetivo del método posicion(e) en el TAD Lista?**  
A) Elimina el elemento e.  
B) Devuelve el índice del primer nodo con dato e.  
C) Devuelve el nodo anterior a e.  
D) Inserta el dato e al final.  

**Pregunta 31 ¿Cuál es el efecto de esta operación?**
```cpp
entrada.seekg(0, ios::end);
int size = entrada.tellg();
```
A) Cierra el archivo tras leerlo.  
B) Borra el contenido.  
C) Calcula el tamaño del archivo en bytes.  
D) Posiciona el puntero al inicio.  

**Pregunta 32 ¿Qué función cumple el método clear() aplicado sobre un flujo?**  
A) Cierra el archivo.  
B) Borra el contenido del archivo.  
C) Elimina los flags de error del flujo.  
D) Resetea la posición del puntero.  

**Pregunta 33 ¿Cuál es la diferencia clave entre una pila y una cola?**  
A) Ambas eliminan elementos por el final.  
B) La cola es LIFO y la pila es FIFO.  
C) La pila es LIFO y la cola es FIFO.  
D) No hay diferencia.  

**Pregunta 34 ¿Cuál es el resultado de *(tabla + 3) si tabla es un puntero a una tabla de enteros?**  
A) Dirección de tabla[3]  
B) Valor en tabla[3]  
C) El contenido de tabla[0]  
D) Error de compilación  

**Pregunta 35 En una pila implementada con tabla dinámica, ¿cuándo se incrementa el tamaño de la tabla?**  
A) Cuando se desapila un elemento.  
B) Cuando el número de elementos es cero.  
C) Cuando el tope alcanza la capacidad máxima.  
D) Nunca, el tamaño es fijo.  

**Pregunta 36 ¿Qué elemento se elimina en una cola clásica (FIFO)?**  
A) El último insertado.  
B) El más antiguo insertado.  
C) Un elemento aleatorio.  
D) El de mayor valor.  

**Pregunta 37 ¿Qué tipo de parámetro requiere esta plantilla?**
```cpp
template <typename T>
T suma(T a, T b) {
  return a + b;
}
```
A) Solo tipos int.  
B) Cualquier tipo con operador +.  
C) Solo clases.  
D) Solo punteros.  

**Pregunta 38 ¿Cuál es la causa más frecuente de segmentation fault en listas dinámicas?**  
A) Reservar demasiada memoria.  
B) Usar delete sin puntero.  
C) Acceder a un nodo a través de puntero NULL.  
D) Insertar al final de la lista.  

**Pregunta 39 ¿Qué sucede con la memoria dinámica si no se ejecuta delete[] tabla;?**  
A) Se libera automáticamente.  
B) Se lanza una excepción en C++.  
C) Se produce fuga de memoria.  
D) Se borra al reiniciar el programa.  

**Pregunta 40 ¿Cuál es el motivo de error en el uso de Lista en esta función?**
```cpp
void insertarInicio(TNodo_Lista* Lista, float valor);
```
A) No se reserva memoria dinámica.  
B) El puntero Lista no se actualiza en el contexto externo.  
C) El tipo float es incompatible.  
D) Se produce segmentación.  

**Pregunta 41 ¿Cuál es el comportamiento de una cola implementada con lista enlazada simple?**  
A) Inserta por el inicio y elimina por el final.  
B) Inserta por el final y elimina por el inicio.  
C) Inserta y elimina siempre por el mismo extremo.  
D) Inserta por cualquier posición.  

**Pregunta 42 ¿Qué error tiene este código para insertar un nodo en una lista dinámica?**
```cpp
void insertar(TNodo_Lista* elementos, float valor) {
  TNodo_Lista* nuevo = new TNodo_Lista;
  nuevo->Datos = valor;
  nuevo->Siguiente = elementos;
  elementos = nuevo;
}
```
A) El puntero elementos debería ser una referencia o puntero a puntero.  
B) nuevo->Datos debería inicializarse a 0.  
C) No se puede usar new en listas.  
D) Siguiente debe ser NULL siempre.  

**Pregunta 43 En una lista simplemente enlazada, ¿qué ocurre si se elimina un nodo sin actualizar el puntero del nodo anterior?**  
A) El nodo se elimina igualmente.  
B) Se produce un error de compilación.  
C) El nodo se pierde pero permanece enlazado.  
D) La lista queda inconsistente.  

**Pregunta 44 ¿Qué implica esta declaración en C++?**
```cpp
template <class T>
class Lista {
  T* datos;
};
```
A) Lista es una clase que solo sirve para enteros.  
B) Lista es una clase genérica que puede almacenar cualquier tipo T.  
C) T debe ser una clase definida previamente.  
D) datos apunta a una estructura genérica con herencia múltiple.  

**Pregunta 45 ¿Qué ocurre si se hace esto?**
```cpp
int* p = NULL;
*p = 10;
```
A) Asigna 10 a la dirección cero.  
B) Da error de compilación.  
C) Se produce una excepción controlada.  
D) Se produce un error en tiempo de ejecución (segmentation fault).  

**Pregunta 46 ¿Qué hace el siguiente método en una pila enlazada?**
```cpp
void desapilar() {
  TNodo_Pila* aux = elementos;
  elementos = elementos->Siguiente;
  delete aux;
}
```
A) Inserta un nuevo nodo al final.  
B) Elimina el tope de la pila.  
C) Borra toda la pila.  
D) Devuelve el último nodo de la pila.  

**Pregunta 47 ¿Qué ocurre si no se actualiza el puntero Fin en una cola dinámica tras desencolar el último elemento?**  
A) Nada, la cola sigue funcionando.  
B) Fin apunta a NULL automáticamente.  
C) Se produce un comportamiento incorrecto al volver a encolar.  
D) Se lanza una excepción por puntero colgante.  

**Pregunta 48 ¿Qué realiza la función mayor() en esta plantilla?**
```cpp
template <class T>
T mayor(T a, T b) {
  return (a > b) ? a : b;
}
```
A) Devuelve el valor más pequeño.  
B) Devuelve el mayor de dos elementos.  
C) Devuelve un puntero.  
D) No compila si T es int.  

**Pregunta 49 ¿Cuál es la forma correcta de recorrer una lista enlazada?**  
A) Usando for sobre los índices.  
B) Usando un puntero auxiliar y while (ptr != NULL).  
C) Usando acceso directo con ptr[i].  
D) Usando punteros a enteros.  

**Pregunta 50 ¿Qué condición se debe cumplir para insertar un nodo en una posición intermedia de una lista?**  
A) Que la lista esté vacía.  
B) Que el puntero anterior esté correctamente referenciado.  
C) Que el nuevo nodo apunte a NULL.  
D) Que el nuevo nodo se inserte al final.  

**Pregunta 51 ¿Qué ocurre si se realiza delete[] sobre un puntero no creado con new[]?**  
A) Se libera memoria correctamente.  
B) Da error de compilación.  
C) Comportamiento indefinido.  
D) Se corrige en tiempo de ejecución.  

**Pregunta 52 ¿Qué representa streampos en C++?**  
A) Un tipo de error.  
B) Un tipo de flujo estándar.  
C) Un entero que indica la posición del puntero de lectura/escritura.  
D) El número de líneas en un archivo.  

**Pregunta 53 ¿Cuál es el resultado de esta expresión si tabla apunta a un array de enteros?**
```cpp
*(tabla + 2)
```
A) Dirección del tercer elemento.  
B) Valor del tercer elemento.  
C) Error por desreferenciar puntero.  
D) Valor del primer elemento.  

**Pregunta 54 ¿Cuál es el uso de seekg(0, ios::end)?**  
A) Mover el puntero al principio del archivo.  
B) Escribir al final del archivo.  
C) Posicionar el puntero de lectura al final.  
D) Borrar el contenido del archivo.  

**Pregunta 55 ¿Qué hace tellg()?**  
A) Retorna el número de caracteres en el archivo.  
B) Muestra el nombre del archivo abierto.  
C) Devuelve la posición actual del puntero de lectura.  
D) Borra el archivo en disco.  

**Pregunta 56 ¿Cuál es el error más común en listas circulares?**  
A) No enlazar el último nodo con el primero.  
B) Insertar nodos duplicados.  
C) Tener nodos con valor NULL.  
D) No usar new al crear un nodo.  

**Pregunta 57 ¿Qué hace ofstream salida("datos.txt", ios::app);?**  
A) Borra el archivo y escribe.  
B) Abre el archivo para lectura.  
C) Abre el archivo para añadir contenido al final.  
D) Crea un archivo temporal.  

**Pregunta 58 ¿Qué ocurre si se llama a eliminar(i) cuando i > longitud()?**  
A) Elimina el último nodo.  
B) No elimina nada.  
C) Se produce un acceso a memoria inválida.  
D) Elimina todos los nodos.  

**Pregunta 59 ¿Cuál es el beneficio principal del uso de const en funciones con punteros?**  
A) Se evita que la función use new.  
B) Se indica que no se modificará el contenido apuntado.  
C) Mejora el rendimiento.  
D) Obliga a pasar punteros por valor.  

**Pregunta 60 ¿Qué es una estructura genérica de tipo lista?**  
A) Una lista implementada en otro lenguaje.  
B) Una clase Lista con plantilla de tipo.  
C) Una lista con punteros a punteros.  
D) Una lista con valores numéricos únicamente.  



**Pregunta 61 ¿Cuál es la principal desventaja de utilizar tablas dinámicas en listas?**  
A) No permiten redimensionado.  
B) El acceso aleatorio es más lento.  
C) El sistema operativo debe mover datos en memoria al redimensionar.  
D) No se pueden liberar con delete.  

**Pregunta 62 ¿Qué condición debe cumplirse para que Anterior(i) devuelva NULL en una lista enlazada?**  
A) La lista está vacía.  
B) El índice es mayor que n.  
C) Se busca el nodo anterior al primero.  
D) Se busca el nodo en la última posición.  

**Pregunta 63 ¿Cuál de las siguientes estructuras no es lineal?**  
A) Lista doblemente enlazada.  
B) Cola circular.  
C) Árbol binario.  
D) Pila con nodos enlazados.  

**Pregunta 64 En una cola circular con tabla dinámica, ¿qué ocurre si fin + 1 == inicio?**  
A) Cola vacía.  
B) Cola llena.  
C) Cola parcialmente llena.  
D) Error de segmentación.  

**Pregunta 65 ¿Qué método en archivos binarios permite modificar datos ya escritos?**  
A) getline()  
B) write() con ios::app  
C) write() tras un seekp()  
D) cin en modo texto  

**Pregunta 66 ¿Cuál es el resultado de esta operación?**
```cpp
float* tabla = new float[3];
tabla[0] = 1.1;
tabla[1] = 2.2;
tabla[2] = 3.3;
cout << *(tabla + 1);
```
A) 1.1  
B) 2.2  
C) 3.3  
D) Dirección de tabla[1]  

**Pregunta 67 ¿Qué se requiere para que una clase pueda ser usada como tipo en una plantilla?**  
A) Tener herencia múltiple.  
B) Definir todos sus miembros como públicos.  
C) Soportar las operaciones utilizadas en la plantilla (ej. >, ==).  
D) Derivar de std::generic.  

**Pregunta 68 ¿Qué significa que new devuelva NULL?**  
A) Que no hay suficientes recursos para ejecutar el programa.  
B) Que se creó correctamente una variable.  
C) Que no se pudo reservar memoria dinámica.  
D) Que se ha ejecutado un destructor.  

**Pregunta 69 ¿Para qué sirve el operador & en punteros?**  
A) Multiplica direcciones de memoria.  
B) Devuelve el contenido de una variable.  
C) Devuelve la dirección de una variable.  
D) Libera la memoria apuntada.  

**Pregunta 70 ¿Cuándo se debe usar delete[] en vez de delete?**  
A) Cuando se libera una clase genérica.  
B) Cuando la memoria fue reservada con new[].  
C) Cuando no se ha usado new.  
D) Siempre que se usen punteros.  

**Pregunta 71 ¿Cuál es la función de gcount() tras una lectura binaria?**  
A) Retorna el número de líneas leídas.  
B) Devuelve los bytes disponibles en el archivo.  
C) Devuelve la cantidad de bytes leídos en la última operación.  
D) Retorna el puntero de lectura al inicio.  

**Pregunta 72 ¿Cuál es la principal diferencia entre ifstream y fstream?**  
A) ifstream puede escribir y leer, fstream solo leer.  
B) ifstream solo lee; fstream permite leer y escribir.  
C) ifstream siempre abre en modo binario.  
D) fstream requiere cerrar el archivo manualmente.  

**Pregunta 73 ¿Qué ocurre si se intenta observar un elemento fuera del rango en observar(i)?**  
A) Devuelve -1.  
B) Devuelve NULL.  
C) Se produce acceso inválido a memoria.  
D) Lanza una excepción.  

**Pregunta 74 ¿Qué ocurre al aplicar delete a un puntero a NULL?**  
A) Se lanza un error.  
B) Se borra el contenido de memoria anterior.  
C) No ocurre nada; es seguro.  
D) El programa se detiene.  

**Pregunta 75 ¿Cuál es la finalidad del método modificar(i, e)?**  
A) Inserta un elemento en posición i.  
B) Devuelve el elemento i.  
C) Sustituye el contenido del nodo i.  
D) Elimina el nodo en i.  

**Pregunta 76 ¿Cuándo es más recomendable usar listas enlazadas en vez de tablas dinámicas?**  
A) Cuando el número de elementos es constante.  
B) Cuando se hacen inserciones frecuentes en el medio de la lista.  
C) Cuando se necesita acceso rápido por índice.  
D) Cuando los elementos son muy grandes.  

**Pregunta 77 ¿Qué ocurre si no se reinicia el puntero Inicio en una cola dinámica después de desencolar el último nodo?**  
A) La cola funciona correctamente.  
B) El siguiente encolar funcionará mal.  
C) El programa lanza una excepción.  
D) Se borra el archivo asociado.  

**Pregunta 78 ¿Cuál es la principal diferencia entre una lista simplemente enlazada y una doblemente enlazada?**  
A) Solo la doble permite recorrer hacia atrás.  
B) Solo la simple permite inserciones en cualquier posición.  
C) Solo la doble permite observar nodos.  
D) Ambas son equivalentes.  

**Pregunta 79 ¿Qué representa el siguiente código?**
```cpp
template <class T>
class Cola {
  T* elementos;
};
```
A) Una clase genérica para pilas.  
B) Una cola que solo funciona con enteros.  
C) Una definición de cola para cualquier tipo T.  
D) Una clase sin funcionalidad.  

**Pregunta 80 ¿Qué hace este código si elementos es NULL?**
```cpp
elementos->Siguiente = nuevo;
```
A) Asigna nuevo como siguiente nodo.  
B) El programa lanza error de segmentación.  
C) Crea una nueva lista.  
D) Enlaza el nodo al final.  



**Pregunta 81 ¿Qué representa este fragmento de código?**
```cpp
template <class T>
TLista<T>::~TLista() {
  TNodo_Datos<T>* aux = elementos, *sig;
  while (aux != NULL) {
    sig = aux->Siguiente;
    delete aux;
    aux = sig;
  }
}
```
A) Destruye la tabla dinámica.  
B) Destruye una lista genérica eliminando nodo a nodo.  
C) Borra los datos pero no los nodos.  
D) No elimina correctamente los punteros.  

**Pregunta 82 ¿Qué devuelve la función esvacia() en una lista?**  
A) true si elementos es NULL.  
B) false si la lista tiene un nodo.  
C) true si n == 0.  
D) true si el puntero al siguiente es NULL.  

**Pregunta 83 ¿Qué indica este constructor?**
```cpp
TLista<T>::TLista() {
  elementos = NULL;
  n = 0;
}
```
A) Inicia la lista con un nodo vacío.  
B) Crea una lista con un solo nodo.  
C) Inicializa la lista como vacía.  
D) La lista apunta a una zona aleatoria de memoria.  

**Pregunta 84 En una lista genérica TLista<T>, ¿qué hace insertar(i, elto)?**  
A) Inserta un nodo con valor elto en la posición i.  
B) Sustituye el nodo de la posición i.  
C) Elimina el nodo i.  
D) Recorre la lista sin modificarla.  

**Pregunta 85 ¿Qué error hay en este código?**
```cpp
void modificar(int i, T elto) {
  TNodo_Datos<T>* ant = Anterior(i), *aux;
  if (ant == NULL)
    aux = elementos;
  else
    aux = ant->Siguiente;
  aux->Datos = elto;
}
```
A) aux puede ser NULL si i está fuera de rango.  
B) Datos no puede modificarse.  
C) elementos debe ser liberado con delete.  
D) Anterior siempre devuelve NULL.  

**Pregunta 86 ¿Cuál es la ventaja de utilizar clases plantilla como TLista<T>?**  
A) Reduce el número de líneas de código.  
B) Aumenta la eficiencia del programa.  
C) Permite reutilizar código para diferentes tipos de datos.  
D) Genera archivos más pequeños.  

**Pregunta 87 ¿Qué hace esta función?**
```cpp
T observar(int i) {
  TNodo_Datos<T>* ant = Anterior(i), *aux;
  aux = (ant == NULL) ? elementos : ant->Siguiente;
  return aux->Datos;
}
```
A) Devuelve la dirección del nodo.  
B) Devuelve el valor almacenado en el nodo i.  
C) Elimina el nodo i.  
D) Inserta un nuevo nodo en i.  

**Pregunta 88 ¿Qué ocurre si Anterior(i) no encuentra un nodo válido?**  
A) Devuelve el último nodo.  
B) Devuelve un puntero colgante.  
C) Devuelve NULL.  
D) Causa error de compilación.  

**Pregunta 89 ¿Cuál es el propósito de posicion(elto)?**  
A) Retornar el índice del nodo con ese dato.  
B) Retornar el nodo anterior al dato.  
C) Eliminar el dato de la lista.  
D) Crear un nuevo nodo con ese dato.  

**Pregunta 90 ¿Qué ocurre en eliminar(i) si Anterior(i) devuelve NULL?**  
A) Se elimina el nodo final.  
B) Se elimina el nodo i+1.  
C) Se elimina el primer nodo.  
D) No se elimina ningún nodo.  

**Pregunta 91 ¿Qué hace esta línea?**
```cpp
template <class T> T mayor(T a, T b);
```
A) Declara una clase.  
B) Declara una función plantilla.  
C) Especializa un tipo.  
D) Sobre-escribe el operador >.  

**Pregunta 92 ¿Cuál es el comportamiento del código?**
```cpp
char* mayor(char* a, char* b) {
  return (strcmp(a, b) > 0) ? a : b;
}
```
A) Compara dos direcciones de memoria.  
B) Devuelve la cadena lexicográficamente mayor.  
C) Devuelve la más corta.  
D) Devuelve la concatenación de ambas.  

**Pregunta 93 ¿Qué tipo de error previene if (b != NULL) al usar new?**  
A) Acceso a memoria ya liberada.  
B) Pérdida de memoria.  
C) Intento de acceso a puntero nulo.  
D) Redefinición de punteros.  

**Pregunta 94 ¿Cuál es la instrucción correcta para reservar un nodo de tipo TNodo_Datos<float>?**  
A) TNodo_Datos<float>* n = new TNodo_Datos;  
B) TNodo_Datos<float> n = new TNodo_Datos<float>;  
C) float* n = new TNodo_Datos<float>;  
D) TNodo_Datos* n = new float;  

**Pregunta 95 En la clase genérica TLista<T>, ¿qué indica que los métodos están en el .h?**  
A) No es válido en C++.  
B) Es obligatorio para plantillas.  
C) Mejora la legibilidad.  
D) Es una convención opcional.  

**Pregunta 96 ¿Por qué los métodos plantilla deben ir en el archivo de cabecera?**  
A) Porque no compilan en .cpp.  
B) Porque deben ser visibles para su instanciación en tiempo de compilación.  
C) Porque solo pueden compilarse con gcc.  
D) Porque así lo requiere la sintaxis de template.  

**Pregunta 97 ¿Qué ocurre si se intenta compilar una clase plantilla y se dejan sus métodos en un .cpp?**  
A) Se genera código duplicado.  
B) El linker no encuentra las definiciones.  
C) El código funciona igual.  
D) No se puede compilar con plantillas.  

**Pregunta 98 ¿Qué ventaja tiene definir template <class T> en estructuras como nodos?**  
A) Ocupa menos memoria.  
B) Permite listas dinámicas de distintos tipos de datos.  
C) Permite insertar valores nulos.  
D) Solo sirve en clases, no estructuras.  

**Pregunta 99 En una lista genérica, ¿qué ocurre si el tipo T no tiene operador ==?**  
A) No se puede usar en posicion(elto).  
B) No se puede insertar datos.  
C) La lista se comporta como si estuviera vacía.  
D) Da error al compilar.  

**Pregunta 100 ¿Qué debe garantizar una clase al ser usada como T en una TLista<T>?**  
A) Tener métodos insertar y eliminar.  
B) Ser hija de TLista.  
C) Tener operador == y operador < definidos si se usan.  
D) Implementar main().  



**Pregunta 101 ¿Qué se obtiene al compilar correctamente una clase plantilla con múltiples tipos de datos?**  
A) Una única versión en código máquina.  
B) Una función genérica para todos los tipos.  
C) Una versión por cada tipo instanciado.  
D) Una clase abstracta.  

**Pregunta 102 ¿Qué condición debe cumplirse para que eliminar(i) funcione correctamente en una lista genérica?**  
A) Que i esté entre 0 y n.  
B) Que i == longitud().  
C) Que 1 ≤ i ≤ n.  
D) Que i sea impar.  

**Pregunta 103 ¿Qué problema resuelve la especialización de plantillas?**  
A) Permite definir estructuras circulares.  
B) Permite definir código específico para tipos concretos.  
C) Permite usar void* en plantillas.  
D) Sustituye las funciones virtuales.  

**Pregunta 104 ¿Qué ventaja ofrece la sobrecarga de plantillas frente a la especialización?**  
A) Es más eficiente en tiempo de ejecución.  
B) Permite definir múltiples versiones con distintos números de argumentos.  
C) Permite usar punteros genéricos.  
D) Reduce el uso de memoria.  

**Pregunta 105 ¿Cuál de las siguientes afirmaciones sobre template<typename T> es verdadera?**  
A) Solo puede usarse con tipos primitivos.  
B) typename y class son equivalentes.  
C) Solo se puede usar con estructuras.  
D) Se debe usar obligatoriamente class.  

**Pregunta 106 ¿Cuál es la ventaja de utilizar listas genéricas sobre listas normales?**  
A) Se reduce el tamaño del ejecutable.  
B) Se mejora la compatibilidad con punteros.  
C) Permite reutilizar código para cualquier tipo sin reescribir la clase.  
D) Solo se pueden usar con tipos primitivos.  

**Pregunta 107 ¿Qué se necesita para que una plantilla funcione correctamente con el operador <?**  
A) Que el tipo base tenga definida la función operator<.  
B) Que el tipo sea una clase derivada.  
C) Que se incluya <algorithm>.  
D) Que sea un tipo numérico.  

**Pregunta 108 ¿Cuál es el resultado del siguiente código si v es una tabla de enteros con al menos 5 elementos?**
```cpp
template <class T>
T mayor(T v[], int dim) {
  T max = v[0];
  for (int i = 1; i < dim; ++i)
    if (v[i] > max)
      max = v[i];
  return max;
}
```
A) Devuelve la posición del mayor.  
B) Devuelve el mayor valor del array.  
C) Devuelve el promedio.  
D) Devuelve siempre v[0].  

**Pregunta 109 ¿Qué indica el siguiente prototipo?**
```cpp
template <class T>
T mayor(T, T, T);
```
A) Una plantilla sobrecargada con tres parámetros.  
B) Una clase con tres operadores.  
C) Un operador ternario.  
D) Un template inválido.  

**Pregunta 110 ¿Qué significa que una plantilla define un conjunto infinito de funciones?**  
A) Puede instanciarse en tiempo de ejecución.  
B) Crea todas las versiones al compilar.  
C) Puede generar tantas versiones como tipos se usen.  
D) Genera código en tiempo real.  

**Pregunta 111 ¿Qué ocurre si un tipo T no tiene definido el operador > en la plantilla mayor<T>?**  
A) Se usa el operador de punteros.  
B) Se genera un error en tiempo de compilación.  
C) Se genera un warning.  
D) Se compila, pero da error en ejecución.  

**Pregunta 112 ¿Cuál es el comportamiento esperado al llamar mayor(c1, c2) con char*?**
```cpp
template <class T>
T mayor(T a, T b) {
  return (a > b) ? a : b;
}
```
A) Compara lexicográficamente las cadenas.  
B) Compara direcciones de memoria.  
C) Lanza una excepción.  
D) Concatena las cadenas.  

**Pregunta 113 ¿Cuál es la forma correcta de especializar una plantilla mayor<T> para char*?**  
A) Usar plantillas parciales.  
B) Usar template<> con una versión propia para char*.  
C) Reescribir la plantilla entera.  
D) No se puede especializar para tipos puntero.  

**Pregunta 114 ¿Qué pasa si strcmp se usa con un puntero nulo?**  
A) Devuelve 0.  
B) Compara como si fueran cadenas vacías.  
C) Provoca un error de segmentación.  
D) Da como resultado negativo.  

**Pregunta 115 ¿Qué función cumple la cabecera template <class T>?**  
A) Declara un parámetro de tipo que se resolverá en tiempo de compilación.  
B) Es una palabra clave reservada para clases abstractas.  
C) Permite usar T como alias de int.  
D) Define una clase específica para punteros.  

**Pregunta 116 ¿Qué ocurre si se usan dos plantillas con la misma firma de tipos?**  
A) Solo se permite una de ellas.  
B) Se produce ambigüedad y error de compilación.  
C) Se compilan las dos sin problema.  
D) Solo se ejecuta la última definida.  

**Pregunta 117 ¿Cuál es el efecto de la siguiente implementación?**
```cpp
template <class T>
T mayor(T a, T b, T c) {
  return mayor(mayor(a, b), c);
}
```
A) Llama a la sobrecarga con 2 parámetros recursivamente.  
B) Compara con operador lógico.  
C) Es un error semántico.  
D) Devuelve la suma de los tres elementos.  

**Pregunta 118 ¿Qué diferencia hay entre una función genérica y una clase genérica?**  
A) Las clases no pueden tener plantillas.  
B) Las funciones genéricas son más eficientes.  
C) Las funciones genéricas se instancian por llamada; las clases, por uso de tipo.  
D) No hay ninguna diferencia real.  

**Pregunta 119 ¿Qué ventaja ofrece la combinación de plantillas y listas dinámicas?**  
A) Evita el uso de punteros.  
B) Permite manipular listas de cualquier tipo sin duplicar código.  
C) Requiere menos memoria que las tablas estáticas.  
D) Permite recorrer en sentido inverso sin esfuerzo.  

**Pregunta 120 ¿Qué debe hacer un tipo T para poder usarse como parámetro en una plantilla que utilice operadores de comparación?**  
A) Sobrecargar dichos operadores (<, >, ==, etc.).  
B) Heredar de una clase base.  
C) Implementar interfaces genéricas.  
D) Incluir una cabecera estándar.  


**Pregunta 121 ¿Qué significa esta definición en C++?**
```cpp
template <class T>
struct TNodo {
  T dato;
  TNodo* siguiente;
};
```
A) Define un nodo genérico para listas.  
B) Solo funciona con listas de enteros.  
C) No puede compilarse sin typename.  
D) Es una clase que hereda de T.  

**Pregunta 122 ¿En qué caso es necesario usar typename en lugar de class al declarar una plantilla?**  
A) Cuando se define una clase en C.  
B) Cuando se declara un tipo dentro de otra plantilla.  
C) Cuando T es de tipo primitivo.  
D) Siempre que se use T.  

**Pregunta 123 ¿Qué error puede producirse al escribir esta plantilla?**
```cpp
template <class T>
T suma(T a, T b) {
  return a + b;
}
```
A) Si T no define operador +.  
B) Si T es un puntero.  
C) Si T es una clase.  
D) Si T es int.  

**Pregunta 124 ¿Qué hace este código?**
```cpp
template <class T>
void mostrar(T a) {
  cout << a << endl;
}
```
A) Muestra el tipo de a.  
B) Imprime el valor de a si tiene operador << definido.  
C) Imprime la dirección de a.  
D) Lanza excepción por tipo desconocido.  

**Pregunta 125 ¿En qué caso la plantilla mayor(T a, T b) no puede usarse?**  
A) Si T no tiene operador <.  
B) Si T es float.  
C) Si T es una clase con operator<.  
D) Si T es char.  

**Pregunta 126 ¿Cuál es la salida de esta función si v = {4, 2, 7, 1}?**
```cpp
mayor(v, 4)
```
A) 7  
B) 4  
C) 1  
D) Error en compilación.  

**Pregunta 127 ¿Qué hace el siguiente fragmento?**
```cpp
template <class T>
class Cola {
  T elementos[100];
  int inicio, fin;
};
```
A) Implementa una cola estática genérica.  
B) Implementa una pila genérica.  
C) Implementa una cola con memoria dinámica.  
D) Implementa una lista circular.  

**Pregunta 128 ¿Qué sucede si no se define el destructor en una clase con punteros dinámicos?**  
A) Se borra todo correctamente.  
B) Los punteros quedan a NULL.  
C) Se produce fuga de memoria.  
D) El compilador lanza un error.  

**Pregunta 129 ¿Qué problema evita el uso de delete al final de ~TLista()?**  
A) Punteros colgantes.  
B) Duplicación de nodos.  
C) Fugas de memoria por no liberar nodos.  
D) Redefinición de variables.  

**Pregunta 130 ¿Para qué sirve la función Anterior(i)?**  
A) Devuelve el dato anterior al índice i.  
B) Devuelve el puntero al nodo anterior al i.  
C) Elimina el nodo en la posición i.  
D) Inserta un nodo al final.  

**Pregunta 131 ¿Qué pasa si se hace delete de un nodo que aún es referenciado por otro?**  
A) Nada, el compilador lo ignora.  
B) Se borra correctamente.  
C) Se provoca acceso inválido al usar el puntero antiguo.  
D) Se lanza una excepción en tiempo de ejecución.  

**Pregunta 132 ¿Qué pasa si se ejecuta delete sin comprobar si el puntero es NULL?**  
A) Error de compilación.  
B) Siempre produce segmentation fault.  
C) Es seguro, delete NULL no hace nada.  
D) El programa se detiene.  

**Pregunta 133 ¿Qué representa este código?**
```cpp
TNodo<T>* aux = elementos;
while (aux != NULL) {
  cout << aux->Datos;
  aux = aux->Siguiente;
}
```
A) Recorre una lista enlazada genérica y la imprime.  
B) Elimina los nodos de una lista.  
C) Llena la lista con datos aleatorios.  
D) Modifica cada nodo con un nuevo dato.  

**Pregunta 134 ¿Qué error común se comete al insertar en listas por referencia?**  
A) No comprobar si el índice existe.  
B) No pasar el puntero como referencia o puntero a puntero.  
C) No usar clases virtuales.  
D) Asignar NULL después de insertar.  

**Pregunta 135 ¿Qué ocurre si se invoca insertar(0, dato)?**  
A) Inserta al principio.  
B) Lanza excepción.  
C) Comportamiento indefinido, el índice debe comenzar en 1.  
D) Inserta al final.  

**Pregunta 136 ¿Qué ocurre si insertar en TLista<T> falla al hacer new TNodo_Datos<T>?**  
A) El programa continúa normalmente.  
B) No se inserta el nodo, posible fuga si no se comprueba.  
C) Se lanza excepción.  
D) Se reinicia la lista.  

**Pregunta 137 ¿Qué propiedad tiene el recorrido iterativo con while (aux != NULL)?**  
A) Es más lento que el recursivo.  
B) Es más claro, pero más costoso.  
C) Es eficiente y evita desbordamiento de pila.  
D) Solo se puede usar con punteros dobles.  

**Pregunta 138 ¿Cuál es la consecuencia de no actualizar elementos al insertar en una lista vacía?**  
A) La lista apunta a basura.  
B) El nodo se pierde.  
C) El primer nodo no se guarda.  
D) Todas las anteriores.  

**Pregunta 139 ¿Qué hace la función longitud()?**  
A) Devuelve el tamaño en memoria.  
B) Cuenta los nodos actuales.  
C) Devuelve un puntero al nodo final.  
D) Calcula la capacidad máxima.  

**Pregunta 140 ¿Qué condición debe verificarse antes de llamar a observar(i)?**  
A) Que el nodo i sea mayor que n.  
B) Que la lista no esté vacía.  
C) Que 1 ≤ i ≤ longitud().  
D) Que el dato exista previamente.  



**Pregunta 141 ¿Cuál es la diferencia entre TNodo_Datos<T>* y TNodo_Datos<float>*?**  
A) Solo el segundo es válido en C++.  
B) El primero es una plantilla; el segundo es una instancia concreta.  
C) Ambos son punteros al mismo tipo.  
D) El segundo usa herencia múltiple.  

**Pregunta 142 ¿Qué hace este código?**
```cpp
TLista<int> L;
L.insertar(1, 5);
```
A) Inserta el número 5 al final.  
B) Inserta 5 en la primera posición de una lista de enteros.  
C) Inserta un nodo con puntero a 5.  
D) No compila sin usar new.  

**Pregunta 143 ¿A qué equivale insertar(1, dato) si la lista está vacía?**  
A) Inserta al final.  
B) Inserta al principio.  
C) No realiza ninguna acción.  
D) Lanza un error.  

**Pregunta 144 ¿Qué ocurre si Anterior(i) devuelve NULL y insertar(i, dato) no lo trata?**  
A) El programa continúa sin insertar.  
B) El nodo se pierde en memoria.  
C) El nuevo nodo no se enlaza correctamente.  
D) Se elimina el nodo anterior.  

**Pregunta 145 ¿Qué control se realiza en insertar(i, e) respecto al índice?**  
A) 0 ≤ i ≤ n.  
B) 1 ≤ i ≤ n + 1.  
C) 1 ≤ i ≤ n.  
D) i debe ser múltiplo de 2.  

**Pregunta 146 ¿Qué problema puede producir eliminar(i) si no se verifica i ≤ longitud()?**  
A) Elimina un nodo no existente.  
B) Borra el primer nodo siempre.  
C) Inserta un nodo nuevo.  
D) Recorre la lista hasta el final.  

**Pregunta 147 ¿Qué significa que posicion(e) devuelva -1?**  
A) Que e está en la primera posición.  
B) Que e no está en la lista.  
C) Que e se ha insertado correctamente.  
D) Que la lista está vacía.  

**Pregunta 148 ¿Cuál es el propósito de bool encontrado = false; en posicion(elto)?**  
A) Acelerar el recorrido.  
B) Evitar acceder a nodos no válidos.  
C) Salir del bucle cuando se encuentra el elemento.  
D) Borrar el nodo duplicado.  

**Pregunta 149 ¿Qué ocurre si observar(i) se usa con i > longitud()?**  
A) Devuelve NULL.  
B) Devuelve el último nodo.  
C) Accede a memoria inválida.  
D) Inserta un nodo vacío.  

**Pregunta 150 ¿Qué garantiza esta instrucción?**
```cpp
if (Nodo_Aux != NULL)
```
A) Que la lista está vacía.  
B) Que se puede acceder al nodo sin error.  
C) Que el nodo contiene datos duplicados.  
D) Que se eliminará correctamente.  

**Pregunta 151 ¿Qué hace esta expresión en C++?**
```cpp
*ptr = valor;
```
A) Asigna valor a la dirección apuntada por ptr.  
B) Declara un puntero.  
C) Multiplica el contenido del puntero por valor.  
D) Compara direcciones de memoria.  

**Pregunta 152 ¿Qué sucede si no se hace delete sobre un objeto creado con new?**  
A) El compilador lo elimina al finalizar.  
B) Se genera una fuga de memoria.  
C) Se borra automáticamente en C++.  
D) Se reinicia el sistema.  

**Pregunta 153 ¿Qué pasa si se hace delete[] sobre un puntero creado con new?**  
A) Se libera correctamente.  
B) Se produce error de compilación.  
C) Comportamiento indefinido.  
D) Se libera parcialmente.  

**Pregunta 154 ¿Qué hace b = new TNodo_Datos<float>;?**  
A) Crea un objeto float.  
B) Crea un puntero a TNodo_Datos de tipo float.  
C) Asigna un valor float a b.  
D) Declara una lista vacía.  

**Pregunta 155 ¿Qué contiene el campo Datos de un nodo genérico?**  
A) Siempre un número entero.  
B) Un puntero a otro nodo.  
C) Un valor de tipo T.  
D) Una dirección física.  

**Pregunta 156 ¿A qué se refiere elementos en una lista genérica?**  
A) Al número de nodos.  
B) Al tipo de datos almacenado.  
C) Al puntero al primer nodo.  
D) Al último valor insertado.  

**Pregunta 157 ¿Qué devuelve esvacia()?**  
A) true si n == 0.  
B) false si la lista está vacía.  
C) true si hay nodos.  
D) El número de nodos vacíos.  

**Pregunta 158 ¿Qué ventaja tiene separar Anterior(i) como función auxiliar?**  
A) Mejora el rendimiento.  
B) Permite usarla en múltiples métodos.  
C) Reduce la visibilidad del dato.  
D) Evita el uso de punteros.  

**Pregunta 159 ¿Qué ocurre si eliminar(i) se llama en una lista de un solo nodo?**  
A) Se elimina ese nodo y elementos pasa a ser NULL.  
B) No elimina el nodo.  
C) Se elimina pero el puntero queda inválido.  
D) Elimina el nodo i+1.  

**Pregunta 160 ¿Qué hace esta línea?**
```cpp
elementos = Nodo_Aux;
```
A) Apunta elementos al último nodo.  
B) Enlaza el nuevo nodo como primero de la lista.  
C) Elimina el nodo anterior.  
D) Inicializa el nodo con valor NULL.  



**Pregunta 161 ¿Qué ocurre si no se inicializa el puntero elementos en el constructor de TLista<T>?**  
A) Se inicializa automáticamente a NULL.  
B) El compilador lo detecta como error.  
C) El puntero contendrá un valor basura.  
D) Se crea una lista vacía correctamente.  

**Pregunta 162 ¿Cuál es el comportamiento de eliminar(i) cuando la lista está vacía?**  
A) Elimina el nodo i.  
B) No hace nada, lista vacía.  
C) Devuelve NULL.  
D) Lanza una excepción.  

**Pregunta 163 ¿Cuál es el objetivo de declarar n como atributo en la clase TLista<T>?**  
A) Almacenar el valor del primer nodo.  
B) Contar cuántos nodos han sido eliminados.  
C) Llevar el control del número de elementos actuales.  
D) Contar los elementos máximos posibles.  

**Pregunta 164 ¿Qué ocurre si se hace cout << *puntero; donde puntero es NULL?**  
A) Se imprime 0.  
B) Se imprime basura.  
C) Se produce un error de segmentación.  
D) Se lanza excepción automática.  

**Pregunta 165 ¿Cuál es la finalidad del operador ->?**  
A) Multiplicar el contenido de dos punteros.  
B) Acceder a un miembro de una estructura desde un puntero.  
C) Comparar dos punteros.  
D) Liberar memoria dinámica.  

**Pregunta 166 ¿Qué diferencia hay entre new T y T t;?**  
A) T t; reserva memoria en heap, new en stack.  
B) new T reserva en heap, T t; en stack.  
C) Ambas reservan en el mismo lugar.  
D) new T solo sirve con arrays.  

**Pregunta 167 ¿Qué ocurre si no se incluye #include <fstream> al trabajar con archivos?**  
A) Nada, compila igual.  
B) El archivo se abre en modo binario por defecto.  
C) Error de compilación por tipos no definidos (ifstream, ofstream).  
D) Solo se puede usar FILE*.  

**Pregunta 168 ¿Qué hace este fragmento?**
```cpp
archivo.seekg(0, ios::end);
int tam = archivo.tellg();
```
A) Posiciona el puntero al principio.  
B) Cierra el archivo.  
C) Calcula el tamaño del archivo en bytes.  
D) Borra el contenido del archivo.  

**Pregunta 169 ¿Qué modo de apertura se debe usar para sobrescribir un archivo binario?**  
A) ios::app  
B) ios::in  
C) ios::out | ios::binary  
D) ios::ate  

**Pregunta 170 ¿Qué hace seekp(pos, ios::beg)?**  
A) Posiciona el puntero de escritura en pos bytes desde el principio.  
B) Lee el contenido desde el final.  
C) Imprime en consola desde pos.  
D) Es equivalente a seekg().  

**Pregunta 171 ¿Qué representa tellp() en flujos de salida?**  
A) Retorna el nombre del archivo.  
B) Devuelve el número de líneas.  
C) Devuelve la posición actual del puntero de escritura.  
D) Devuelve la extensión del archivo.  

**Pregunta 172 ¿Qué tipo de acceso realiza archivo.read((char*)&x, sizeof(x));?**  
A) Acceso secuencial en modo texto.  
B) Escritura binaria.  
C) Lectura binaria directa.  
D) Lectura con conversión automática.  

**Pregunta 173 ¿Qué tipo de archivo se usa con ifstream archivo("datos.dat", ios::binary);?**  
A) Archivo de texto.  
B) Archivo de acceso secuencial.  
C) Archivo binario.  
D) Archivo estructurado.  

**Pregunta 174 ¿Cuál es la diferencia entre read() y getline()?**  
A) read() es solo para texto.  
B) getline() trabaja a nivel binario.  
C) read() permite acceder por bytes; getline() por líneas.  
D) Ambas hacen lo mismo.  

**Pregunta 175 ¿Qué hace archivo.clear(); tras un fallo de lectura?**  
A) Borra el contenido del archivo.  
B) Restablece el flujo eliminando flags de error.  
C) Reinicia el archivo desde cero.  
D) Cierra automáticamente el archivo.  

**Pregunta 176 ¿Qué ocurre si se usa write() con un puntero a una clase mal alineado?**  
A) Se produce un error de compilación.  
B) Se corrige automáticamente.  
C) El contenido escrito puede ser incorrecto.  
D) No afecta en C++.  

**Pregunta 177 ¿Cuál es la ventaja del acceso directo frente al secuencial en archivos?**  
A) Permite recorrer más rápidamente línea a línea.  
B) Permite acceder directamente a cualquier posición del archivo.  
C) Reduce el tamaño del archivo.  
D) No requiere open().  

**Pregunta 178 ¿Qué implica abrir un archivo con ios::trunc?**  
A) Se posiciona al final.  
B) Se borra el contenido existente al abrir.  
C) Se vuelve de solo lectura.  
D) Solo se permite escribir al final.  

**Pregunta 179 ¿Cuál es la utilidad del sizeof() en acceso binario?**  
A) Obtener el número de líneas del archivo.  
B) Determinar el tamaño de los datos a escribir o leer.  
C) Saber la ruta del archivo.  
D) Calcular el número de caracteres visibles.  

**Pregunta 180 ¿Qué ocurre si no se cierra un archivo con .close()?**  
A) Se pierde el contenido en RAM.  
B) El archivo no se guarda.  
C) El sistema puede cerrar automáticamente, pero es mala práctica.  
D) El compilador lanza error.  



**Pregunta 181 ¿Qué hace este fragmento en una lista genérica?**
```cpp
TLista<T> L;
L.eliminar(L.longitud());
```
A) Elimina el primer nodo.  
B) Elimina el último nodo.  
C) Borra todos los nodos.  
D) Lanza excepción.  

**Pregunta 182 ¿Cuál es el resultado esperado si se ejecuta modificar(1, e) sobre lista vacía?**  
A) Inserta e en la primera posición.  
B) Se lanza un error de segmentación.  
C) Elimina e.  
D) Modifica el nodo NULL.  

**Pregunta 183 ¿Qué hace el método observar(i)?**  
A) Devuelve el valor almacenado en el nodo i.  
B) Inserta un nuevo nodo en i.  
C) Elimina el nodo i.  
D) Devuelve el puntero al nodo i.  

**Pregunta 184 ¿Cuál es el comportamiento esperado de insertar(n+1, dato)?**  
A) Inserta al final de la lista.  
B) Reemplaza el último nodo.  
C) Elimina el último nodo.  
D) Recorre toda la lista sin insertar.  

**Pregunta 185 ¿Qué significa que Anterior(1) retorne NULL?**  
A) El nodo anterior no existe porque 1 es la primera posición.  
B) Hay un error en la lista.  
C) El nodo 1 es inválido.  
D) El nodo 1 es el último.  

**Pregunta 186 ¿Qué tipo de estructura se adapta mejor al TAD Cola?**  
A) Lista doblemente enlazada.  
B) Tabla circular.  
C) Árbol binario.  
D) Vector ordenado.  

**Pregunta 187 ¿Qué ocurre si Fin->Siguiente no se pone a NULL al eliminar en una cola dinámica?**  
A) No se libera correctamente la memoria.  
B) La cola queda en bucle.  
C) El puntero a NULL permanece válido.  
D) No afecta al funcionamiento.  

**Pregunta 188 ¿Cuál de las siguientes estructuras garantiza acceso en tiempo constante a sus extremos?**  
A) Lista doblemente enlazada.  
B) Tabla dinámica.  
C) Cola circular con punteros a inicio y fin.  
D) Pila recursiva.  

**Pregunta 189 ¿Qué ventaja tiene usar typedef o using en listas genéricas?**  
A) Hace el código más rápido.  
B) Reduce el uso de memoria.  
C) Mejora la legibilidad y reutilización de tipo.  
D) Obliga a usar clases.  

**Pregunta 190 ¿Qué se necesita para que una clase Persona funcione con TLista<Persona>?**  
A) Definir operator< y operator==.  
B) Heredar de TLista.  
C) Incluir main() en la clase.  
D) Declarar todos los miembros como públicos.  

**Pregunta 191 ¿Qué pasa si se usa read() sin haber abierto el archivo?**  
A) Lee desde memoria aleatoria.  
B) Da error de compilación.  
C) El flujo está en modo inválido, no se lee nada.  
D) Se borra el archivo  

**Pregunta 192 ¿Para qué sirve seekg(sizeof(T) * (i - 1), ios::beg)?**  
A) Borrar el elemento i.  
B) Insertar un nuevo nodo en posición i.  
C) Posicionar el puntero de lectura justo antes del registro i.  
D) Calcular el tamaño del archivo.  

**Pregunta 193 ¿Cuál es el objetivo de una estructura genérica como TNodo<T>?**  
A) Permitir que los datos del nodo sean de cualquier tipo.  
B) Reducir el número de punteros usados.  
C) Garantizar acceso constante.  
D) Crear nodos de tipo int únicamente.  

**Pregunta 194 ¿Qué hace este código?**
```cpp
archivo.seekp(0, ios::end);
archivo.write((char*)&x, sizeof(x));
```
A) Lee el valor x.  
B) Inserta x al principio.  
C) Escribe x al final del archivo.  
D) Borrar x del archivo.  

**Pregunta 195 ¿Cuál es la forma correcta de acceder al campo edad de un objeto cliente apuntado por ptr?**  
A) ptr.edad  
B) *ptr.edad  
C) ptr->edad  
D) (*ptr)->edad  

**Pregunta 196 ¿Cuál es la causa más probable de error en esta operación?**
```cpp
archivo.read((char*)&p, sizeof(p));
```
A) p no ha sido declarado.  
B) El archivo no está abierto correctamente.  
C) sizeof(p) es negativo.  
D) read() no puede usarse con estructuras.  

**Pregunta 197 ¿Qué error lógico produce la siguiente implementación?**
```cpp
void insertar(TNodo* Lista, float valor) {
  TNodo* nuevo = new TNodo;
  nuevo->Datos = valor;
  nuevo->Siguiente = Lista;
  Lista = nuevo;
}
```
A) Siguiente no apunta a NULL.  
B) Lista no se actualiza en el entorno de llamada.  
C) valor no se copia correctamente.  
D) nuevo no se inicializa.  

**Pregunta 198 ¿Qué condición se usa habitualmente para recorrer una lista enlazada?**  
A) for (i = 0; i < n; ++i)  
B) while (ptr != NULL)  
C) do { ... } while (ptr != NULL)  
D) ptr == &lista  

**Pregunta 199 ¿Qué implica usar delete sobre un nodo de una lista sin actualizar el anterior?**  
A) Se borra correctamente.  
B) La lista se mantiene enlazada.  
C) El puntero anterior queda colgando.  
D) Se borra el nodo anterior también.  

**Pregunta 200 ¿Qué representa conceptualmente la estructura TAD?**  
A) Un algoritmo que opera sobre arrays.  
B) Una implementación específica en C++.  
C) Una abstracción que define operaciones y comportamiento de un tipo de dato.  
D) Un tipo de archivo de acceso binario.  



**Soluciones y Explicaciones (Preguntas 1–200)**
C – El puntero elementos es pasado por valor; los cambios no afectan al original
C – Uso correcto de new para crear una tabla dinámica
C – Los nodos enlazados permiten inserciones/borrados sin mover otros elementos
C – Lectura directa con desplazamiento calculado mediante seekg
C – write sobrescribe, no inserta
C – El puntero externo original sigue apuntando a zona liberada
B – Se usa acceso directo al final del archivo para consultar su tamaño
C – Sintaxis correcta para crear objeto dinámico e invocar constructor por defecto
B – ifstream se usa para lectura de archivos
B – Modifica el dato en la posición i
C – -> accede a miembro de clase apuntada por puntero
B – En pilas dinámicas, el tope está en el primer nodo
C – Se produce memory leak si no se libera con delete
C – Las plantillas permiten programar sin especificar tipo concreto
C – Devuelve el nodo anterior al que ocupa la posición i
C – Puede comprobarse con .fail() si no se abre correctamente
A – Falla por no proporcionar argumento en la llamada a plantilla
B – Las listas dobles permiten recorrido en ambas direcciones
A – Al pasar Lista por valor, no se refleja el cambio en el puntero original
B – Cola es una estructura FIFO: primero en entrar, primero en salir
C – Si new falla y se accede directamente, se produce acceso inválido
C – Se necesita un contador para distinguir si está llena o vacía
C – Las plantillas evitan duplicar código para distintos tipos
B – esvacia() comprueba si la lista está vacía
D – ios::app escribe al final sin borrar
C – El comportamiento es indefinido al usar delete mal
B – Sobrescribe directamente el elemento i
D – No hay error, es una sobrecarga válida para char*
C – class y typename son equivalentes en plantillas
B – Retorna la posición del primer nodo cuyo valor es e
C – tellg() retorna la posición del puntero = tamaño archivo
C – clear() elimina flags de error en el flujo
C – Pila = LIFO; Cola = FIFO
B – *(tabla + 3) accede al valor de tabla[3]
C – Cuando el tope alcanza el tamaño actual, se redimensiona
B – FIFO: el primero en entrar es el primero en salir
B – Se requiere que el tipo tenga operador + definido
C – Acceder a NULL->Siguiente produce segment fault
C – No liberar la memoria provoca fuga
B – Lista no se pasa como referencia ni doble puntero
B – Inserta al final y elimina al inicio (FIFO)
A – Se modifica solo la copia local del puntero
D – El nodo anterior sigue apuntando al eliminado
B – Plantilla que permite usar cualquier tipo T
D – Acceder a NULL causa error en tiempo de ejecución
B – Elimina el primer nodo, que actúa como tope
C – Fin debe ponerse a NULL si la cola queda vacía
B – Devuelve el mayor de dos elementos
B – Puntero auxiliar y recorrido con while hasta NULL
B – Necesario acceder correctamente al nodo anterior
C – Puede liberar mal la memoria, comportamiento indefinido
C – Indica posición en flujo (lectura o escritura)
B – Accede al valor de tabla[2]
C – Mueve el puntero de lectura al final
C – tellg() devuelve posición del puntero de entrada
A – La propiedad circular se rompe si no se enlaza el último con el primero
C – Añade contenido sin borrar el archivo existente
C – Puede acceder a un puntero NULL o fuera de rango
B – Protege los datos apuntados de modificación
B – Lista parametrizada por tipo T con template
C – Al redimensionar, el sistema debe mover los datos en memoria
C – El nodo anterior al primero es NULL
C – Los árboles no son estructuras lineales
B – Cuando fin alcanza a inicio, la cola circular está llena
C – Para sobrescribir se usa seekp() seguido de write()
B – Se accede al segundo valor del array: 2.2
C – La clase debe soportar las operaciones usadas en la plantilla
C – Indica que no se pudo reservar memoria
C – &x da la dirección de x
B – Se usa delete[] para memoria reservada con new[]
C – gcount() devuelve los bytes realmente leídos
B – ifstream es solo lectura; fstream permite lectura y escritura
C – Se accede a memoria inválida si i excede el rango
C – delete NULL es seguro y no hace nada
C – Sustituye el valor del nodo en la posición i
B – Listas enlazadas son eficientes para inserciones en posiciones intermedias
B – Si Inicio no se pone a NULL, la siguiente operación fallará
A – Solo la doble permite recorrer en ambos sentidos
C – Clase genérica de cola parametrizada por tipo
B – Acceder a NULL->campo produce segmentation fault
B – Elimina uno a uno los nodos de la lista genérica
C – esvacia() devuelve true si n == 0
C – Inicializa lista vacía (NULL y n=0)
A – Inserta el dato elto en posición i
A – Si i es inválido, aux será NULL y se accede a memoria inválida
C – Las plantillas permiten reutilizar el código con tipos distintos
B – Devuelve el valor del nodo en la posición i
C – Anterior(i) retorna NULL si i == 1 o si no hay nodo anterior
A – Busca el nodo que contiene elto y devuelve su posición
C – Si no hay nodo anterior, se elimina el primero
B – Se trata de la declaración de una función plantilla
B – Devuelve la mayor cadena usando strcmp
C – Verifica que el puntero no sea NULL antes de usarlo
A – Sintaxis correcta para reservar nodo genérico
B – Los métodos deben estar en el .h para que el compilador genere código al instanciar
B – Las plantillas se instancian en tiempo de compilación, requieren visibilidad
B – El linker no encuentra definiciones de métodos si no están en el .h
B – Permite listas de cualquier tipo de dato
A – No se podrá comparar elementos correctamente en posicion(elto)
C – Debe soportar los operadores usados por la clase (como ==, <, etc.)
C – El compilador genera una versión por cada tipo usado
C – Se define solo si 1 ≤ i ≤ longitud()
B – Permite definir comportamiento específico para un tipo concreto
B – La sobrecarga permite diferentes números de argumentos
B – class y typename son intercambiables al declarar plantillas
C – Evita duplicación de código, útil para reutilización
A – El tipo debe definir el operador < si se va a usar en la plantilla
B – Devuelve el mayor elemento del array usando >
A – Una sobrecarga de plantilla con tres argumentos del mismo tipo
C – Puede instanciarse para cualquier tipo compatible en tiempo de compilación
B – Se produce error de compilación si el operador no está definido
B – Compara direcciones, no contenidos, si no se especializa
B – Se debe usar template<> para definir una versión específica para char*
C – strcmp(NULL, x) produce error de segmentación
A – Declara un parámetro de tipo genérico
B – Dos plantillas con firma idéntica causan ambigüedad
A – Aplica recursivamente mayor(a, b) y luego compara con c
C – Las funciones se instancian por uso; clases, por declaración de objetos
B – Permite manipular listas de cualquier tipo sin duplicar código
A – Debe implementar los operadores requeridos para compilar correctamente
A – Declara un nodo genérico con dato y puntero al siguiente
B – Se usa typename al declarar tipos anidados en plantillas
A – Error si el tipo no tiene operador + definido
B – Solo imprime si operator<< está definido para T
A – Si T no tiene operator<, la plantilla falla
A – Devuelve el mayor valor: 7
A – Cola genérica con tamaño fijo de 100 elementos
C – No liberar memoria causa memory leaks
C – delete en destructor evita fugas de nodos
B – Devuelve puntero al nodo anterior al índice i
C – El puntero siguiente queda colgando y su uso puede fallar
C – delete NULL es seguro y no hace nada
A – Recorre e imprime todos los nodos de una lista
B – Si no se pasa por referencia, el puntero original no se actualiza
C – El índice mínimo permitido es 1
B – Si no se comprueba NULL, se puede perder el nodo y causar errores
C – Iterativo evita problemas de stack overflow en listas grandes
D – No actualizar elementos causa múltiples errores lógicos
B – Retorna n, el número de nodos actuales
C – Se debe comprobar que el índice esté entre 1 y longitud
B – El primero es una plantilla; el segundo, una instancia concreta
B – Inserta el número 5 en la posición 1 de la lista de enteros
B – Inserta al principio de la lista
C – Si no se enlaza con elementos, el nodo queda aislado
B – El índice debe estar entre 1 y n+1 para permitir inserción válida
A – Se accede a nodos inexistentes, provocando errores de acceso
B – Devuelve -1 cuando el elemento no está presente en la lista
C – Se usa como condición de parada en el recorrido
C – El índice está fuera de rango, se accede a memoria inválida
B – Protege el acceso al puntero evitando fallos si es NULL
A – Asigna valor a la dirección contenida en el puntero
B – Produce una fuga de memoria (memory leak)
C – Solo debe usarse delete[] si se usó new[], si no, comportamiento indefinido
B – Reserva memoria para un nodo de tipo float y asigna su dirección a b
C – Guarda un valor del tipo T especificado en la plantilla
C – Es el puntero al primer nodo de la lista genérica
A – Devuelve true si el número de nodos es cero (n == 0)
B – Facilita reutilización en métodos como insertar, modificar, eliminar
A – El único nodo se elimina y el puntero elementos queda en NULL
B – Se establece el nuevo nodo como inicio de la lista
C – Sin inicialización, contiene basura; puede causar errores
B – No realiza nada porque no hay nodos que eliminar
C – n guarda el número de elementos actuales en la lista
C – Desreferenciar puntero NULL da segmentation fault
B – Accede a miembro de una estructura apuntada
B – new reserva en heap; declaración simple en stack
C – Tipos como ifstream, ofstream requieren <fstream>
C – Calcula tamaño del archivo situando puntero al final y usando tellg()
C – ios::out | ios::binary sobrescribe archivo binario desde el principio
A – Sitúa puntero de escritura desde el inicio del archivo
C – Devuelve posición del puntero de escritura actual
C – Lectura binaria mediante read() usando conversión a char*
C – Archivo abierto en modo binario para lectura
C – read() opera por bytes, getline() por líneas (modo texto)
B – clear() limpia flags de error como eof, fail, etc.
C – Puede generar escritura incorrecta por mala alineación de memoria
B – Acceso directo permite saltar a cualquier posición del archivo
B – ios::trunc borra el contenido al abrir el archivo
B – Permite saber cuántos bytes ocupa el dato para usar en read/write
C – Aunque el sistema puede cerrarlo, es mala práctica no usar .close()
B – Elimina el último nodo (n) de la lista
B – Acceder a nodo inexistente produce error de segmentación
A – Devuelve el valor del nodo en posición i
A – Inserta al final de la lista si i == n + 1
A – No existe nodo anterior al primero, por eso retorna NULL
B – La cola circular permite un uso eficiente de memoria y control de inicio/fin
B – Si Fin->Siguiente no apunta a NULL, se forma bucle infinito
C – Con punteros a inicio y fin, el acceso es constante (O(1))
C – using o typedef mejora legibilidad de estructuras genéricas
A – Debe tener definidos los operadores usados por la lista (==, <, etc.)
C – El flujo está en estado inválido, la operación read() no hace nada
C – Posiciona puntero justo antes del registro i
A – Permite listas donde los nodos contienen cualquier tipo de dato
C – Escribe el contenido de x al final del archivo binario
C – ptr->edad es acceso correcto al campo de una clase apuntada
B – Si el archivo no está abierto, read() no funciona
B – Lista es un parámetro por valor, no se actualiza fuera de la función
B – La condición típica es while (ptr != NULL)
C – El puntero al nodo borrado sigue usándose en el anterior, queda colgando
C – Un TAD define el comportamiento abstracto de un tipo de dato
