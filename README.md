# 🐚 Bash Essentials

Una guía completa y práctica para aprender Bash desde cero, con comandos esenciales, ejercicios progresivos y scripts reales.

## 📖 ¿Qué encontrarás aquí?

Esta guía está diseñada para llevarte desde los comandos más básicos de Bash hasta la creación de scripts automatizados en **4 semanas**. Cada comando viene con:

- ✅ Descripción clara y concisa
- ✅ Ejemplos prácticos
- ✅ Ejercicios para practicar
- ✅ Proyectos reales

## 🎯 ¿Para quién es esta guía?

- Principiantes que nunca han usado la terminal
- Desarrolladores que quieren automatizar tareas
- Estudiantes de informática o sistemas
- Cualquiera que quiera dominar Linux/Unix

## 📚 Contenido Principal

### **[📄 BASH_GUIDE.md](BASH_GUIDE.md)**
La guía completa con todos los comandos, ejercicios y proyectos organizados por semanas.

**Incluye:**
- Comandos de navegación
- Manipulación de archivos
- Búsqueda con `grep` y `find`
- Pipes y redirección
- Scripts automatizados
- Variables y bucles
- Funciones en Bash
- Proyectos finales

## 📊 Plan de Aprendizaje (4 Semanas)

| Semana | Tema | Estado |
|--------|------|--------|
| **Semana 1** | Comandos básicos y navegación | 🔄 En progreso |
| **Semana 2** | Variables, condicionales y bucles | ⏳ Pendiente |
| **Semana 3** | Funciones y manejo de archivos | ⏳ Pendiente |
| **Semana 4** | Scripts avanzados y automatización | ⏳ Pendiente |

## 🛠️ Requisitos Previos

### Para Windows (Recomendado: WSL)

Si usas **Windows**, te recomiendo instalar **WSL (Windows Subsystem for Linux)** para tener un entorno Linux real.

#### 📥 Instalación de WSL en Windows 10/11

**Método 1: Instalación Automática (Recomendado)**

1. Abre **PowerShell** o **CMD** como **Administrador**
   - Click derecho en el botón de Windows
   - Selecciona "Terminal (Admin)" o "Windows PowerShell (Admin)"

2. Ejecuta el siguiente comando:
   ```powershell
   wsl --install
   ```

3. Reinicia tu computadora cuando se te solicite

4. Después del reinicio, se abrirá automáticamente Ubuntu
   - Crea tu usuario de Linux
   - Crea tu contraseña (no se mostrará mientras escribes, es normal)

5. ¡Listo! Ya tienes Ubuntu en Windows

---

**Método 2: Instalación Manual (Windows 10 versiones antiguas)**

1. Habilitar WSL:
   ```powershell
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
   ```

2. Habilitar la plataforma de máquina virtual:
   ```powershell
   dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
   ```

3. Reinicia tu PC

4. Descargar e instalar el paquete de actualización del kernel de Linux:
   - Ve a: https://aka.ms/wsl2kernel
   - Descarga e instala el paquete

5. Establece WSL 2 como versión predeterminada:
   ```powershell
   wsl --set-default-version 2
   ```

6. Instala Ubuntu desde Microsoft Store:
   - Abre Microsoft Store
   - Busca "Ubuntu"
   - Click en "Obtener" o "Instalar"
   - Abre Ubuntu y configura tu usuario

---

**Verificar instalación:**

```bash
# Ver versión de WSL
wsl --version

# Ver distribuciones instaladas
wsl --list --verbose

# Debería mostrar Ubuntu con VERSION 2
```

---

**Comandos útiles de WSL:**

```powershell
# Iniciar WSL
wsl

# Listar distribuciones instaladas
wsl --list

# Apagar WSL
wsl --shutdown

# Actualizar WSL
wsl --update

# Establecer Ubuntu como predeterminada
wsl --set-default Ubuntu
```

---

#### 🖥️ Terminal Recomendada: Warp

**Warp** es una terminal moderna, rápida y con autocompletado inteligente.

**Instalación:**
1. Descarga desde: https://www.warp.dev/
2. Instala normalmente
3. Abre Warp y selecciona WSL como tu shell

**Alternativas:**
- **Windows Terminal** (Microsoft Store - Gratuita)
- **Hyper** (https://hyper.is/)
- Terminal nativa de Ubuntu (viene con WSL)

---

### Para macOS

macOS ya viene con Bash instalado. Solo abre la aplicación **Terminal**.

```bash
# Verificar versión de Bash
bash --version
```

---

### Para Linux

Si ya usas Linux, ¡perfecto! Solo abre tu terminal favorita.

```bash
# Verificar versión de Bash
bash --version
```

---

## 🚀 Cómo Usar Esta Guía

### 1. **Configura tu entorno**
   - Instala WSL (si usas Windows)
   - Abre tu terminal

### 2. **Abre la guía principal**
   - Lee [BASH_GUIDE.md](BASH_GUIDE.md)
   - Sigue el plan semana por semana

### 3. **Practica cada comando**
   - No solo leas, ¡escribe los comandos!
   - Haz los ejercicios propuestos
   - Crea tus propios scripts

### 4. **Completa los proyectos**
   - Al final de cada semana hay un proyecto
   - Los proyectos integran todo lo aprendido

### 5. **Marca tu progreso**
   - Usa los checkboxes de la guía
   - Celebra cada logro ✅

---

## 📂 Estructura del Repositorio

```
bash-essentials/
├── README.md              # Este archivo (introducción y setup)
├── BASH_GUIDE.md          # Guía completa de comandos y ejercicios
├── ejercicios/            # Ejercicios organizados por semana
│   ├── semana1/
│   ├── semana2/
│   ├── semana3/
│   └── semana4/
├── scripts/               # Scripts de ejemplo y práctica
└── proyectos/             # Proyectos finales
```

---

## 💡 Consejos para Aprender Mejor

1. **Practica todos los días** (aunque sea 30 minutos)
2. **Escribe los comandos tú mismo** (no copies y pegues)
3. **Experimenta y rompe cosas** (así se aprende)
4. **Haz los ejercicios antes de ver las soluciones**
5. **Crea tus propios scripts** para automatizar tareas reales
6. **Documenta tu código** con comentarios

---

## 🤝 Contribuciones

¿Encontraste un error? ¿Tienes una sugerencia? ¡Las contribuciones son bienvenidas!

1. Haz fork del repositorio
2. Crea una rama para tu feature (`git checkout -b feature/mejora`)
3. Commit tus cambios (`git commit -m 'Add: nueva sección'`)
4. Push a la rama (`git push origin feature/mejora`)
5. Abre un Pull Request

---

## 📝 Licencia

Este proyecto es de código abierto y está disponible para uso educativo.

---

## 👤 Autor

**Edwin Granada** ([@edwingran](https://github.com/edwingran))

Mi viaje aprendiendo programación desde cero. Si te sirve esta guía, ¡dale una ⭐ al repo!

---

## 🔗 Recursos Adicionales

- [Bash Guide for Beginners](https://tldp.org/LDP/Bash-Beginners-Guide/html/)
- [Explainshell](https://explainshell.com/) - Explica cualquier comando
- [ShellCheck](https://www.shellcheck.net/) - Valida tus scripts
- [Bash Cheat Sheet](https://devhints.io/bash)

---

## 📊 Progreso Actual

- ✅ Configuración inicial del repositorio
- ✅ Comandos básicos de navegación
- ✅ Manipulación de archivos
- 🔄 Ejercicios de práctica (en progreso)

---

**¡Empieza tu viaje en Bash ahora! Abre [BASH_GUIDE.md](BASH_GUIDE.md) y comienza con la Semana 1.** 🚀

---

_Última actualización: Enero 2026_
