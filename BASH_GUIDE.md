# 📚 Bash - GUIDE

**Autor:** jegacode  
**Inicio:** Enero 2026  
**Última actualización:** 05/01/2026

---

## 📋 Primeros Comandos

### Navegación
| Comando | Descripción |
|---------|-------------|
| `pwd` | Muestra el directorio actual (Print Working Directory) |
| `cd` | Cambia de directorio (Change Directory) |
| `cd ..` | Sube un nivel en la estructura de directorios |
| `cd ~` | Va al directorio home del usuario |
| `cd -` | Vuelve al directorio anterior |
| `ls` | Lista archivos y directorios |
| `ls -l` | Lista con detalles (permisos, propietario, tamaño, fecha) |
| `ls -la` | Lista TODO incluyendo archivos ocultos |

### Manipulación de Archivos y Directorios
| Comando | Descripción |
|---------|-------------|
| `mkdir` | Crea un directorio |
| `mkdir -p` | Crea directorios anidados (ejemplo: `mkdir -p dir1/dir2/dir3`) |
| `touch` | Crea un archivo vacío o actualiza fecha de modificación |
| `cp` | Copia archivos (ejemplo: `cp origen.txt destino.txt`) |
| `mv` | Mueve o renombra archivos |
| `rm` | Elimina archivos |
| `rm -r` | Elimina directorios recursivamente |
| `tree` | Muestra estructura de directorios en forma de árbol |

### Visualización de Contenido
| Comando | Descripción |
|---------|-------------|
| `cat` | Muestra todo el contenido de un archivo |
| `echo` | Imprime texto en la terminal |
| `head` | Muestra las primeras 10 líneas de un archivo |
| `head -n 3` | Muestra las primeras 3 líneas (cambiar número según necesidad) |
| `tail` | Muestra las últimas 10 líneas de un archivo |
| `tail -n 2` | Muestra las últimas 2 líneas |
| `wc` | Cuenta líneas, palabras y caracteres de un archivo |

### Redirección
| Comando | Descripción |
|---------|-------------|
| `>` | Redirige output a archivo (sobrescribe) |
| `>>` | Redirige output a archivo (agrega al final) |
| `|` | Pipe - conecta la salida de un comando con la entrada de otro |

### Búsqueda
| Comando | Descripción |
|---------|-------------|
| `grep "palabra" archivo.txt` | Busca texto dentro de un archivo |
| `grep -i` | Búsqueda sin distinción de mayúsculas/minúsculas |
| `grep -n` | Muestra número de línea donde encuentra coincidencias |
| `find . -name "*.txt"` | Busca archivos por nombre |
| `find practica/ -type d` | Busca solo directorios |
| `find practica/ -type f` | Busca solo archivos |

### Permisos
| Comando | Descripción |
|---------|-------------|
| `chmod +x archivo.sh` | Da permisos de ejecución a un script |

### Otros
| Comando | Descripción |
|---------|-------------|
| `whoami` | Muestra el usuario actual |
| `date` | Muestra la fecha y hora actual |

---

## 🎯 Ejercicios Completados

### ✅ Ejercicio 1: Navegación Básica
**Objetivo:** Practicar comandos de navegación

```bash
pwd           # ¿Dónde estoy?
ls            # ¿Qué hay aquí?
ls -la        # Ver TODO (incluso archivos ocultos)
cd ..         # Subir un nivel
cd ~          # Ir a home
cd -          # Volver al directorio anterior
```

---

### ✅ Ejercicio 2: Crear Estructura de Archivos
**Objetivo:** Crear directorios y archivos

**Estructura deseada:**
```
practica/
  ├── documentos/
  │   ├── archivo1.txt
  │   └── archivo2.txt
  ├── imagenes/
  └── videos/
```

**Comandos usados:**
```bash
mkdir -p practica/{documentos,imagenes,videos}
touch practica/documentos/archivo1.txt
touch practica/documentos/archivo2.txt
tree practica
```

---

### ✅ Ejercicio 3: Manipulación Básica
**Objetivo:** Copiar, mover y renombrar archivos

```bash
# Copiar archivo
cp practica/documentos/archivo1.txt practica/documentos/copia.txt

# Mover archivo
mv practica/documentos/copia.txt practica/imagenes/

# Renombrar
mv practica/imagenes/copia.txt practica/imagenes/nuevo_nombre.txt

# Ver contenido
echo "Hola Mundo" > practica/documentos/saludo.txt
cat practica/documentos/saludo.txt
```

---

### 🔄 Ejercicio 4: Trabajar con Contenido de Archivos
**Objetivo:** Crear archivos con múltiples líneas y visualizar contenido

```bash
# Crear archivo con múltiples líneas
echo "Línea 1: Bash es genial" > practica/documentos/prueba.txt
echo "Línea 2: Estoy aprendiendo" >> practica/documentos/prueba.txt
echo "Línea 3: Comandos de Linux" >> practica/documentos/prueba.txt
echo "Línea 4: WSL funciona bien" >> practica/documentos/prueba.txt
echo "Línea 5: Warp es rápido" >> practica/documentos/prueba.txt

# Ver todo el contenido
cat practica/documentos/prueba.txt

# Ver solo las primeras 3 líneas
head -n 3 practica/documentos/prueba.txt

# Ver solo las últimas 2 líneas
tail -n 2 practica/documentos/prueba.txt

# Contar líneas, palabras y caracteres
wc practica/documentos/prueba.txt
```

**Nota importante:**
- `>` sobrescribe el archivo (borra contenido anterior)
- `>>` agrega al final sin borrar (append)

---

### 🔄 Ejercicio 5: Búsqueda con grep
**Objetivo:** Buscar texto dentro de archivos

```bash
# Buscar la palabra "aprendiendo" en el archivo
grep "aprendiendo" practica/documentos/prueba.txt

# Buscar sin importar mayúsculas/minúsculas
grep -i "bash" practica/documentos/prueba.txt

# Buscar en todos los archivos .txt del directorio
grep "Línea" practica/documentos/*.txt

# Buscar y mostrar número de línea
grep -n "Warp" practica/documentos/prueba.txt
```

---

### 🔄 Ejercicio 6: Uso de find
**Objetivo:** Buscar archivos y directorios

```bash
# Buscar todos los archivos .txt en practica/
find practica/ -name "*.txt"

# Buscar directorios
find practica/ -type d

# Buscar solo archivos
find practica/ -type f

# Buscar archivos que contengan "nuevo" en el nombre
find practica/ -name "*nuevo*"
```

---

### 🔄 Ejercicio 7: Pipes (Combinar Comandos)
**Objetivo:** Conectar comandos usando pipes

```bash
# Listar archivos y contar cuántos hay
ls practica/documentos/ | wc -l

# Listar archivos y buscar los que contienen "archivo"
ls practica/documentos/ | grep "archivo"

# Ver contenido y buscar una palabra específica
cat practica/documentos/prueba.txt | grep "Bash"

# Listar todos los .txt y ordenarlos
find practica/ -name "*.txt" | sort
```

---

### 🔄 Mini Proyecto: Script de Organización
**Objetivo:** Crear un script que organice archivos por extensión

**Archivo:** `organizar.sh`

```bash
#!/bin/bash

# Script que organiza archivos por extensión
# Autor: jegacode
# Fecha: 2026-01-02

echo "==================================="
echo "Organizador de Archivos por Tipo"
echo "==================================="
echo ""

# Crear directorios para diferentes tipos
mkdir -p archivos_organizados/{textos,scripts,otros}

# Copiar archivos .txt
echo "Copiando archivos .txt..."
find practica/ -name "*.txt" -exec cp {} archivos_organizados/textos/ \;

# Copiar archivos .sh
echo "Copiando archivos .sh..."
find . -name "*.sh" -exec cp {} archivos_organizados/scripts/ \;

echo ""
echo "✅ Organización completada!"
echo ""
echo "Resumen:"
echo "Textos encontrados: $(find archivos_organizados/textos/ -type f | wc -l)"
echo "Scripts encontrados: $(find archivos_organizados/scripts/ -type f | wc -l)"
```

**Para ejecutar:**
```bash
chmod +x organizar.sh
./organizar.sh
tree archivos_organizados/
```

---

### 🎯 Reto Pendiente: Script de Backup
**Objetivo:** Crear un script que haga backup de archivos .txt

**Requisitos:**
1. Crear directorio llamado `backup_[fecha]`
2. Copiar todos los archivos .txt de `practica/` al backup
3. Mostrar mensaje de cuántos archivos copió
4. Listar el contenido del backup

**Estructura básica:**
```bash
#!/bin/bash

# Variables
FECHA=$(date +%Y%m%d_%H%M%S)
DIR_BACKUP="backup_$FECHA"

# Crear directorio
# Copiar archivos
# Mostrar resumen
```

---

## 📊 Progreso Semana 1

### ✅ Completado (~40%)
- [x] Navegación básica (pwd, cd, ls)
- [x] Creación de archivos y directorios
- [x] Copiar, mover, renombrar
- [x] Visualización con cat
- [x] Redirección básica (>, >>)

### 🔄 En Progreso (~60%)
- [ ] grep avanzado
- [ ] find con diferentes opciones
- [ ] Pipes (|)
- [ ] head, tail, wc
- [ ] Scripts más complejos

---

## 💡 Conceptos Clave Aprendidos

### Diferencia entre `>` y `>>`
- `>` → Sobrescribe el archivo completamente
- `>>` → Agrega contenido al final del archivo

### Diferencia entre `cp` y `mv`
- `cp` → Copia el archivo (original permanece)
- `mv` → Mueve o renombra (original desaparece)

### ¿Para qué sirve `chmod +x`?
- Da permisos de ejecución a un script
- Sin esto, el script no se puede ejecutar con `./script.sh`

---

## 🔗 Recursos Útiles

- **WSL** - Windows Subsystem for Linux
- **Warp** - Terminal moderna
- **tree** - Comando para visualizar estructura de directorios

---

_Este documento se irá actualizando conforme avance en el aprendizaje._
