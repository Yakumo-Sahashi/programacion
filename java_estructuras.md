# Java – Estructuras de Datos y Sus Métodos Más Importantes

---

# LIST & ARRAYLIST
Estructura dinámica, ordenada y permite duplicados.

## Métodos principales
- add(element)
- add(index, element)
- get(index)
- set(index, element)
- remove(index)
- remove(Object o)
- size()
- clear()
- contains(element)
- indexOf(element)
- isEmpty()

### Ejemplo completo
```java
List<String> lista = new ArrayList<>();

lista.add("Hola");
lista.add("Mundo");
lista.add(1, "Java");

System.out.println(lista.get(0)); // Hola

lista.set(1, "Programación");

lista.remove("Hola");
lista.remove(0);

System.out.println(lista); // [Programación]
```

---

# LINKEDLIST
Lista doblemente enlazada. Eficiente en inserciones y borrados.

## Métodos principales
- addFirst(element)
- addLast(element)
- getFirst()
- getLast()
- removeFirst()
- removeLast()

### Ejemplo
```java
LinkedList<Integer> numeros = new LinkedList<>();

numeros.addFirst(10);
numeros.addLast(20);

System.out.println(numeros.getFirst()); // 10
System.out.println(numeros.getLast());  // 20

numeros.removeFirst(); // elimina 10
```

---

# SET (HashSet, TreeSet)
Colección sin duplicados.

## Métodos principales
- add(element)
- remove(element)
- contains(element)
- size()
- clear()
- isEmpty()

## Operaciones matemáticas entre sets
```java
Set<Integer> A = new HashSet<>(Arrays.asList(1,2,3));
Set<Integer> B = new HashSet<>(Arrays.asList(3,4,5));

// Unión
Set<Integer> union = new HashSet<>(A);
union.addAll(B); // [1,2,3,4,5]

// Intersección
Set<Integer> inter = new HashSet<>(A);
inter.retainAll(B); // [3]

// Diferencia
Set<Integer> dif = new HashSet<>(A);
dif.removeAll(B); // [1,2]
```

---

# MAP (HashMap, TreeMap)
Almacena pares clave → valor.

## Métodos principales
- put(key, value)
- get(key)
- getOrDefault(key, defaultValue)
- containsKey(key)
- containsValue(value)
- remove(key)
- size()
- clear()
- isEmpty()
- keySet()
- values()
- entrySet()

### Ejemplo completo
```java
Map<String, Integer> persona = new HashMap<>();

persona.put("edad", 20);
persona.put("anio", 2025);

int edad = persona.get("edad");
int salario = persona.getOrDefault("salario", 0);

persona.remove("anio");

for (Map.Entry<String, Integer> entry : persona.entrySet()) {
    System.out.println(entry.getKey() + " : " + entry.getValue());
}
```

---

# ARRAYS EN JAVA
Estructura fija y estática.

## Funciones útiles con Arrays (import java.util.Arrays;)
- Arrays.sort(arr)
- Arrays.binarySearch(arr, value)
- Arrays.fill(arr, value)
- Arrays.copyOf(arr, newLength)
- Arrays.equals(arr1, arr2)
- Arrays.toString(arr)

### Ejemplo
```java
int[] nums = {3, 1, 2};
Arrays.sort(nums); // [1, 2, 3]

int pos = Arrays.binarySearch(nums, 2); // 1

Arrays.fill(nums, 9);  // [9, 9, 9]
```

---

# COLECCIONES (java.util.Collections)
Funciona sobre cualquier colección de Java.

## Métodos útiles
- Collections.sort(list)
- Collections.reverse(list)
- Collections.shuffle(list)
- Collections.max(list)
- Collections.min(list)

### Ejemplo
```java
List<Integer> lista = Arrays.asList(3, 1, 2);

Collections.sort(lista);      // [1,2,3]
Collections.reverse(lista);   // [3,2,1]
Collections.shuffle(lista);   // orden aleatorio
```

---

# ITERADORES
Muy útil para recorrer colecciones evitando errores de modificación.

## Ejemplo de uso
```java
List<String> lista = new ArrayList<>(Arrays.asList("A","B","C"));

Iterator<String> it = lista.iterator();
while (it.hasNext()) {
    System.out.println(it.next());
}
```
