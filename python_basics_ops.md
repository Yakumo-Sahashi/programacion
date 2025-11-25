
# Funciones Útiles y Conceptos Básicos Importantes en Python

---

# Operaciones Básicas en Python

## Operadores aritméticos
- **+** suma  
- **-** resta  
- **\*** multiplicación  
- **/** división  
- **//** división entera  
- **%** módulo  
- **\*\*** potencia  

### Ejemplo
```python
a = 10
b = 3
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```

---

## Operadores lógicos
- **and**
- **or**
- **not**

```python
x = True
y = False
print(x and y)  # False
```

---

## Operadores relacionales
- ==  
- !=  
- >  
- <  
- >=  
- <=  

---

# Funciones Integradas Útiles

## type()
```python
type(5)        # int
type("hola")   # str
```

## input()
```python
nombre = input("Ingresa tu nombre: ")
```

## print()
```python
print("Hola", nombre)
```

## range()
```python
for i in range(5):
    print(i)
```

## isinstance()
```python
isinstance(5, int)  # True
```

---

# Estructuras de control

## if – elif – else
```python
if x > 0:
    print("positivo")
elif x == 0:
    print("cero")
else:
    print("negativo")
```

## for
```python
for i in [1,2,3]:
    print(i)
```

## while
```python
while x < 5:
    x += 1
```

---

# Manejo básico de archivos
```python
with open("archivo.txt", "r") as f:
    contenido = f.read()
```
