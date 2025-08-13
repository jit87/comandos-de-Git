# 🧠 Guía de Comandos Básicos de Git

Una recopilación de los comandos esenciales para trabajar con Git en entornos locales y remotos.

---

## 📌 COMANDOS BÁSICOS

### 🔄 Añadir y confirmar cambios en el repositorio local
```bash
git add .
git commit -m "Mensaje de confirmación"
```

### 👤 Configurar identidad del usuario
```bash
git config --global user.email "tu@email.com"
git config --global user.name "Tu Nombre"
```

### 📋 Ver estado del repositorio
```bash
git status
```

### 🔁 Fusionar cambios del repositorio remoto con el local
```bash
git pull --allow-unrelated-histories URL main
```

### 🌿 Crear una nueva rama y cambiar a ella
```bash
git checkout -b main
```

### 🔍 Verificar el repositorio remoto
```bash
git remote -v
```

### 🗑️ Eliminar una rama local
```bash
git branch -d nombre-rama
```

---

### FUSIONAR RAMAS

Pasos para fusionar dos ramas en Git

1. Ir a la rama destino (la que recibirá los cambios):

   ```bash
   git checkout main
   ```
3. Actualizar la rama destino con el remoto:
   ```bash
   git pull origin main
   ```
5. Fusionar la rama origen (la que tiene los cambios, en este caso la llamamos 'develop'):
   ```bash
   git merge develop
   ```

7. Resolver conflictos (solo si los hay):
   - Editar los archivos marcados por Git.
   - Marcar como resueltos:
     ```bash
     git add <archivo>
     ```
   - Confirmar la resolución:
     ```bash
     git commit
     ```

8. Subir los cambios fusionados al remoto:
   ```bash
   git push origin main
   ```
---

## 🧯 Recuperación y control de versiones

### 📜 Ver historial de commits
```bash
git log
git log --oneline
```

### ♻️ Recuperar archivos eliminados
```bash
git checkout <id_del_commit> .
```

### ⏪ Volver a un commit anterior (elimina cambios posteriores)
```bash
git reset --hard <hash_del_commit>
```

### ⏳ Volver atrás N commits
```bash
git reset --hard HEAD~N
```

---

## 🧹 Limpieza y ajustes

### 🗃️ Eliminar archivo del repositorio (mantenerlo en local)
```bash
git rm --cached nombre_archivo
```

### 🛑 Evitar que un archivo siga subiendo (por error en .gitignore)
```bash
git rm --cached ruta_archivo
```

### ⚠️ Forzar que el repositorio remoto sea igual al local
```bash
git push --force origin main
```

---

## 🔍 Búsqueda

### 📂 Buscar un archivo específico por nombre
```bash
find . -name "nombre_archivo"
```

---

## 🚀 SUBIR PROYECTO LOCAL A REPOSITORIO REMOTO

### Opción 1: Paso a paso
```bash
git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/USUARIO/NOMBRE_REPOSITORIO.git
git push -u origin main
```

### Opción 2: Alternativa con set-upstream
```bash
git push --set-upstream origin main
```

---

## 💬 MENSAJE DE COMMIT EN VI (terminal Bash)

1. Pulsa `i` para insertar texto  
2. Escribe tu mensaje de merge  
3. Pulsa `ESC`  
4. Escribe `:wq` y pulsa `Enter` para guardar y salir  

---

## 📥 CLONAR UN REPOSITORIO
```bash
git clone https://github.com/usuario/nombre-repositorio.git
cd nombre-repositorio
git status
```
