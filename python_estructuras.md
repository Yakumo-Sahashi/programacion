# Python – Estructuras de Datos y Métodos Más Importantes

---

# LISTAS (`list`)
Estructura **mutable**, ordenada y permite elementos duplicados.

## Métodos principales
- **append(x)** – Agrega un elemento al final  
  ```python
  lista.append(10)
  ```
- **insert(i, x)** – Inserta un elemento en la posición indicada  
  ```python
  lista.insert(2, "hola")
  ```
- **extend(iterable)** – Agrega múltiples elementos  
  ```python
  lista.extend([4, 5, 6])
  ```
- **remove(x)** – Elimina la primera coincidencia  
  ```python
  lista.remove(3)
  ```
- **pop(i)** – Elimina y regresa un elemento (default: último)  
  ```python
  lista.pop()     # último elemento
  lista.pop(1)    # posición 1
  ```
- **clear()** – Vacía toda la lista  
- **sort()** – Ordena la lista  
  ```python
  lista.sort(reverse=True)
  ```
- **reverse()** – Invierte el orden  
- **count(x)** – Cuenta cuántas veces aparece  
- **index(x)** – Regresa la primera posición del elemento

## Funciones integradas útiles
- **len(lista)** – Longitud  
- **min(lista)**  
- **max(lista)**  
- **sum(lista)**  
  ```python
  sum([1,2,3])  # 6
  ```

---

# TUPLAS (`tuple`)
Estructura **inmutable**, ordenada.

## Métodos disponibles
- **count(x)**  
- **index(x)**

## Operaciones útiles
- **Concatenación**  
  ```python
  t3 = t1 + t2
  ```
- **Desempaquetado**
  ```python
  a, b, c = (1, 2, 3)
  ```

---

# SETS (`set`)
Colección **sin orden**, **sin duplicados**.

## Métodos principales
- **add(x)** – Agrega un elemento  
  ```python
  s.add(10)
  ```
- **update(iterable)** – Agrega múltiples  
  ```python
  s.update([1, 2, 3])
  ```
- **remove(x)** – Elimina (error si no existe)  
- **discard(x)** – Elimina (sin error si no existe)  
- **pop()** – Elimina elemento aleatorio  
- **clear()**

## Operaciones matemáticas entre sets
- **Unión**
  ```python
  A | B
  ```
- **Intersección**
  ```python
  A & B
  ```
- **Diferencia**
  ```python
  A - B
  ```
- **Diferencia simétrica**
  ```python
  A ^ B
  ```

---

# DICCIONARIOS (`dict`)
Estructura de pares **clave → valor**.

## Métodos útiles
- **get(clave, default)**  
  ```python
  persona.get("edad", 0)
  ```
- **keys()** – Regresa solo las claves  
- **values()** – Regresa solo los valores  
- **items()** – Regresa tuplas (clave, valor)  
- **update(dict)** – Mezcla diccionarios  
- **pop(clave)** – Elimina y obtiene valor  
- **popitem()** – Elimina el último par  
- **setdefault(clave, default)** – Si no existe, asigna  
- **clear()**

### Ejemplo completo
```python
persona = {"nombre": "Leo", "edad": 20}
persona["ciudad"] = "CDMX"
persona.update({"edad": 21})
valor = persona.pop("ciudad")
```

---

# Funciones Útiles Para Cualquier Iterable

## enumerate()
Obtiene índice y valor.
```python
for i, v in enumerate(["a","b","c"]):
    print(i, v)
```

## zip()
Combina iterables.
```python
for a, b in zip([1,2], ["x","y"]):
    print(a, b)
```

## sorted()
Devuelve una **nueva** lista ordenada.
```python
sorted([3,1,2])  # [1,2,3]
```

## map()
Aplica una función a cada elemento.
```python
list(map(lambda x: x*2, [1,2,3]))
```

## filter()
Filtra elementos según una condición.
```python
list(filter(lambda x: x > 2, [1,2,3,4]))
```

## reduce()  
(Se importa desde `functools`)
```python
from functools import reduce
reduce(lambda a,b: a+b, [1,2,3])  # 6
```