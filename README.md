# Práctica Recuperacion GitHub y Markdown

> **Nota** Durante el intento de arreglar el error de verificacion de credenciales que no me permitia actualizar el proyecto en mi repositorio, encontre **GitHub CLI (`gh`)**, lo instalé y configuré, me permitió vincular mi cuenta de forma sencilla y sin tener que introducir ninguna credencial de mi cuenta de github y poder trabajar desde mi terminal directamente sobre el repositorio.

## 1: Creación del repositorio

Primero he creado un repositorio en GitHub llamado:

```
ExamenRecuperacionED
```

He marcado la opción de añadir un archivo README inicial.

---

## 2: Clonado del repositorio

Desde la terminal, he clonado el repositorio a mi equipo con el siguiente comando:

```bash
git clone https://github.com/angelandres27/ExamenRecuperacionED.git
cd ExamenRecuperacionED
```

Después he comprobado el estado del repositorio:

```bash
git status
git branch
```

Esto me mostró que estaba en la rama principal main.

---

## 3: Creación de una rama de funcionalidad

He creado una nueva rama para trabajar sin afectar a la principal:

```bash
git checkout -b feature-lista
```

Después he creado un archivo llamado `lista.txt`:

```bash
touch lista.txt
```

Y he añadido esto:

```
- Manzana
- Pan
- Leche
```

Luego he guardado los cambios con:

```bash
git add .
git commit -m "Lista de la compra hecha"
```

Intenté subir los cambios con:

```bash
git push origin feature-lista
```

---

## 4: Merge a la rama principal

He vuelto a la rama principal:

```bash
git checkout main
```

Y he hecho el merge de la rama creada:

```bash
git merge feature-lista
```

---

## 5: Corrección en otra rama

Para simular una corrección, he creado otra rama:

```bash
git checkout -b fix-typo
```

He modificado el archivo `lista.txt`, cambiando por ejemplo:

```
Pan → Pan integral
```

Después he hecho commit:

```bash
git add .
git commit -m "Tipo de pan"
```

---

## 6: Uso de Markdown

En este mismo archivo README he utilizado Markdown para documentar el proceso.

### Ejemplos usados:

* `#` para títulos
* `##` para subtítulos
* `-` para listas
* `bash` para bloques de código

---
