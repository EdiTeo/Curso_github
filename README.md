# Curso GitHub
# Clase 1 – Introducción al Control de Versiones y Git

## ¿Qué es un control de versiones?
Un sistema que registra cada cambio que se realiza en el código fuente de un proyecto. Permite:

- Llevar un historial completo de modificaciones.
- Saber quién hizo qué y cuándo.
- Revertir errores fácilmente.
- Trabajar en equipo sin conflictos.

## Importancia de un control de versiones
- 🔁 **Seguimiento de cambios:** puedes ver y revertir cualquier modificación.
- 🤝 **Colaboración eficiente:** varios desarrolladores trabajando al mismo tiempo.
- 🔒 **Seguridad:** conserva la integridad de los archivos.
- 🔄 **Flexibilidad:** no necesitas un desarrollo lineal.

---

## Historia breve

| Año  | Evento                                                        |
|------|---------------------------------------------------------------|
| 1990 | Nace CVS, cada archivo tenía su propia versión con un número. |
| 2005 | Linus Torvalds crea Git tras la caída de BitKeeper.          |
| 2008 | Se crea GitHub con Ruby on Rails.                             |
| 2018 | Microsoft compra GitHub.                                      |
| 2024 | Git sigue dominando el mercado (GitHub, GitLab, Bitbucket).   |

---

## ¿Qué es Git?

Git es un **sistema de control de versiones distribuido**. Cada desarrollador tiene una copia completa del proyecto (repositorio) en su equipo.

Permite:

- Trabajar sin conexión.
- Realizar commits y pruebas locales antes de compartir cambios.
- Rastrear todo el historial del proyecto de forma segura.

---

## ¿Qué es un repositorio?

Un repositorio es el **almacén donde se guardan los archivos del proyecto y su historial**. 

📚 Metáfora: Es como una estantería con libros, donde cada libro representa una versión diferente del proyecto.

---

## Algunos otros sistemas de control de versiones

- 🔹 GitLab
- 🔹 Bitbucket
- 🔹 Mercurial
- 🔹 Bazaar

---

## Tipos de sistemas de control de versiones

### 📁 Local
Cada desarrollador guarda los cambios en su máquina local. No permite colaboración fácil.

### 🌐 Centralizado
Un servidor central contiene el proyecto. Todos los usuarios dependen de la conexión al servidor (ej. SVN, CVS).

### 🌍 Distribuido
Cada usuario tiene una copia local del repositorio. Ejemplo: **Git**

---

## Iniciando un proyecto en Git

### 🔸 Desde cero:
```bash
git init nombre-de-tu-proyecto
cd nombre-de-tu-proyecto
```

### 🔸 En una carpeta existente:
```bash
cd carpeta-existente
git init
```

---

## Los 3 estados de Git

| Estado    | Descripción                                                                 |
|-----------|-----------------------------------------------------------------------------|
| Modified  | Archivo creado, eliminado o modificado pero sin agregar para commit.       |
| Staged    | Archivo listo para ser guardado (commit).                                  |
| Committed | Archivo ya guardado en el repositorio local.                               |

---

## Cambiar de estado

1. Ver el estado actual:
```bash
git status
```

2. Pasar archivo a la etapa de **Staged**:
```bash
git add README.md
```

3. Guardar cambios (hacer commit):
```bash
git commit
```
Se abrirá un editor donde debes escribir el mensaje del commit. Luego guarda y cierra.

4. Ver el historial de commits:
```bash
git log
```

---

## ¿Qué es un Commit?

Un **punto de guardado** que captura el estado actual del proyecto.

Contiene:

- Fecha
- Autor
- Mensaje descriptivo
- Archivos afectados

✅ Para hacer un commit, los archivos deben estar en estado **Staged**.

---

## ¿Qué es el HEAD?

`HEAD` es un **puntero que indica en qué commit estás actualmente**.

Se puede ver con:
```bash
git log
```

Ejemplo:
```
commit bd68fe7a12bedcff7f3330ec376ec1dfea2fad4b (HEAD -> main)
Author: Sebastian Barrera <correo@ejemplo.com>
Date:   Sun May 5 18:20:18 2024 -0400
```

---

## Comandos útiles de Git

| Comando | Descripción |
|--------|-------------|
| `git add .` | Agrega todos los archivos al área de preparación (Staged). |
| `git rm <archivo>` | Elimina el archivo del área de preparación. |
| `git commit -m "mensaje"` | Hace commit sin abrir editor. |
| `git commit --amend -m "nuevo mensaje"` | Cambia el mensaje del último commit. |
| `git commit -am "mensaje"` | Agrega y hace commit de todos los archivos rastreados. |
| `git checkout <id_commit>` | Cambia el HEAD a un commit anterior. |
