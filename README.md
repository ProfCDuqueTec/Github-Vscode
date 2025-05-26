# Github-Vscode
````markdown
# Cheat Sheet Profesional: Publicación y Actualización de Proyectos C++ en GitHub

## 1. Publicación Inicial en GitHub

Antes de empezar, asegúrate de tener tu proyecto estructurado en VS Code (con carpetas `include/`, `src/`, `tests/`, etc.)
y haber instalado Git en tu equipo.

---

### Paso 1: Inicializar el repositorio local

```bash
cd /ruta/a/tu/proyecto
git init
````

* Crea el directorio oculto `.git/` con toda la información de control de versiones.

---

### Paso 2: Configurar archivos de soporte

1. **`.gitignore`**
   Incluye al menos:

   ```gitignore
   /build/
   *.exe
   *.o
   .vscode/
   .devcontainer/
   ```
2. **`README.md`**

   * Título y descripción breve
   * Instrucciones de compilación y ejecución
   * Ejemplos de uso

---

### Paso 3: Primer **commit**

```bash
git add .
git commit -m "Inicializar proyecto C++ con estructura profesional"
```

* Incluye TODO el contenido de tu proyecto listo para compartirse.

---

### Paso 4: Crear el repositorio remoto

* En GitHub: ➞ **New repository**

  * Nombre: `cpp-polymorphism-demo` (por ejemplo)
  * Tipo: Public o Private
  * **No** marques “Initialize with README”

* Copia la URL SSH o HTTPS que GitHub te muestra.

---

### Paso 5: Enlazar y subir

```bash
git remote add origin <URL-del-repositorio>
git branch -M main
git push -u origin main
```

* `main` será tu rama principal por defecto.
* El flag `-u` asocia tu rama local con `origin/main`.

---

### Paso 6: Verificación final

* Abre `https://github.com/<TuUsuario>/<NombreRepo>`
* Confirma que aparezcan todos los archivos y carpetas.

---

## 2. Actualización Continua

Cada vez que realices cambios en VS Code:

---

### Paso 1: Guardar tus cambios

* Pulsa **Ctrl + S** o usa **Archivo → Guardar todo**.

---

### Paso 2: Revisar el estado

```bash
git status
```

* Identifica archivos modificados, nuevos o eliminados.

---

### Paso 3: Preparar (stage) los cambios

* Para todo:

  ```bash
  git add .
  ```
* Para archivos específicos:

  ```bash
  git add src/Example.cpp include/Example.h
  ```

---

### Paso 4: Crear un commit significativo

```bash
git commit -m "Descripción clara del cambio realizado"
```

* Usa verbo imperativo y mensaje breve pero descriptivo.

---

### Paso 5: Subir al remoto

```bash
git push
```

* Si es la primera vez en una nueva rama:

  ```bash
  git push -u origin <rama>
  ```

---

### Paso 6: Confirmación en GitHub

* Visita la pestaña **Commits** de tu repositorio
* Asegúrate de que tu último mensaje aparece con fecha y hora correctas

---

## 3. Buenas Prácticas

* **Sincroniza antes de trabajar**:

  ```bash
  git pull --rebase
  ```
* **Usa ramas feature/** para nuevas funcionalidades y PRs para integrarlas.
* **Protege `main`** con reglas de branch protection y revisiones obligatorias.
* **Documenta** cada cambio en el mensaje del commit y en el **CHANGELOG.md**.

---

> Este documento resume un flujo profesional, claro y reproducible para gestionar tus proyectos C++ en GitHub desde VS Code. ¡Listo para compartir con tu equipo!

```
```
