# Curso GitHub
 
<details>
  <summary><strong>📘 Clase 1 – Introducción al Control de Versiones y Git</strong></summary>

<br>
<h2 align="center">¿Qué es un control de versiones?</h2>

El control de versiones es un sistema que registra los cambios realizados sobre un archivo o conjunto de archivos a lo largo del tiempo de tal manera que sea posible recuperar versiones especificas más adelante. Permite:
 
- ✅ Llevar un historial completo de modificaciones.<br>
- 👤 Saber quién hizo qué y cuándo.<br>
- 🔄 Revertir errores fácilmente.<br>
- 🤝 Trabajar en equipo sin conflictos.<br>
   
<p align="center">
<img src="img/control_version.png" alt="Control version local" width="60%">
</p>
 
Los sistemas de control de versiones han ido evolucionando a lo largo del tiempo y podemos clasificarlos en tres tipos: **Locales**, **Centralizados** y **Distribuidos**.

 ### <p align="center"><strong>📁 Sistemas de Control de Versiones Locales</strong></p>

Los sistemas locales almacenaban versiones en bases de datos en lugar de múltiples archivos. Solo se tenía una copia activa del proyecto, evitando confusión o eliminación de versiones.

<p align="center">
<img src="img/v_local.png" alt="Control version local" width="60%">
</p>

👉 Se trabajaba en el computador personal del desarrollador, sin una forma eficiente de compartir el código.

### <p align="center"><strong>🌐 Sistemas de Control de Versiones Centralizados</strong></p>

Para facilitar la colaboración, se comenzó a usar un servidor central donde se almacenaban los cambios y versiones.

<p align="center">
<img src="img/v_centralizado.png" alt="Control version Centralizado" width="60%">
</p>

📌 Problema: conflictos al editar el mismo archivo.<br>
🛠️ Solución: gestionar conflictos manualmente.<br>
😰 Limitación: ineficiente en equipos grandes con actualizaciones frecuentes.<br>

### <p align="center"><strong>🌍 Sistemas de Control de Versiones Distribuidos</strong></p>

Cada desarrollador tiene una copia local completa del proyecto.

<p align="center">
  <img src="img/v_distribuido.png" alt="Control version Distribuido" width="60%">
</p>

🔄 Trabaja localmente sin depender de un servidor.
✅ Más seguro ante caídas del servidor.
🤝 Mejor resolución de conflictos y trabajo simultáneo.

---

## <h2 align="center">Importancia de un control de versiones</h2>

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

 ## <h2 align="center">¿Qué es Git?</h2>

Git es un **sistema de control de versiones distribuido**. Cada desarrollador tiene una copia completa del proyecto (repositorio) en su equipo.

Permite:

- Trabajar sin conexión.
- Realizar commits y pruebas locales antes de compartir cambios.
- Rastrear todo el historial del proyecto de forma segura.

---

## <h2 align="center">¿Qué es un repositorio?</h2>

Un repositorio es el **almacén donde se guardan los archivos del proyecto y su historial**. 

📚 Metáfora: Es como una estantería con libros, donde cada libro representa una versión diferente del proyecto.

<div align="center">
  <a href="" title="Estante de Libros">
    <img src="/img/estante_libros.png?sanitize=true" width="300" height="280" aria-hidden="true">
  </a>
</div>

---
## <h2 align="center">Iniciando un proyecto en Git</h2>

1. Crear el repositorio en GitHub (sin README, `.gitignore`, ni licencia).
<p align="center"> <img src="gif/crear_new_repos.gif" alt="Crear repositorio en GitHub" width="70%"> </p>

2. Clonar el repositorio:
```bash
git clone https://github.com/usuario/nombre-del-repo.git
cd nombre-del-repo
```
3. Agregar tus archivos y hacer el primer commit:
```bash
git add .
git commit -m "feat: proyecto base inicial"
```
4. Subir los cambios a GitHub:
```bash
git push origin main
```


---

## <h2 align="center">Los 3 estados de Git</h2>

| Estado    | Descripción                                                                 |
|-----------|-----------------------------------------------------------------------------|
| Modified  | Archivo creado, eliminado o modificado pero sin agregar para commit.       |
| Staged    | Archivo listo para ser guardado (commit).                                  |
| Committed | Archivo ya guardado en el repositorio local.                               |

---

## <h2 align="center">Cambiar de estado</h2>

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

4. Ver todo el historial de commits:
```bash
git log
```
 Te mostrara lo siguiente: 
 <img src="img/salida_git_log.png" alt="alt text" width="500" height="auto">


---

## <h2 align="center">¿Qué es un Commit?</h2>

Un **punto de guardado** que captura el estado actual del proyecto.

Contiene:

- Fecha
- Autor
- Mensaje descriptivo
- Archivos afectados

✅ Para hacer un commit, los archivos deben estar en estado **Staged**.

---

## <h2 align="center">¿Qué es el HEAD?</h2>

`HEAD` es un **puntero que indica en qué commit estás actualmente**.

Se puede ver con:
```bash
git log
```

Ejemplo:
<img src="img/head_apunta.png" alt="alt text" width="500" height="auto"> 

---

## <h2 align="center">Comandos útiles de Git</h2>

| Comando | Descripción |
|--------|-------------|
| `git add .` | Agrega todos los archivos al área de preparación (Staged). |
| `git rm <archivo>` | Elimina el archivo del área de preparación. |
| `git commit -m "mensaje"` | Hace commit sin abrir editor. |
| `git commit --amend -m "nuevo mensaje"` | Cambia el mensaje del último commit. |
| `git commit -am "mensaje"` | Agrega y hace commit de todos los archivos rastreados. |
| `git checkout <id_commit>` | Cambia el HEAD a un commit anterior. |


</details>
