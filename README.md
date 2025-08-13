# Guía de Comandos Básicos de Git

## 1. Comandos básicos

**Añadir y confirmar cambios en el repositorio local**
```bash
git add .
git commit -m "Mensaje de confirmación"
```

**Configurar identidad del usuario**
```bash
git config --global user.email "tu@email.com"
git config --global user.name "Tu Nombre"
```

**Ver estado del repositorio**
```bash
git status
```

**Fusionar cambios del repositorio remoto con el local**
```bash
git pull --allow-unrelated-histories URL main
```

**Crear una nueva rama y cambiar a ella**
```bash
git checkout -b nombre-rama
```

**Verificar el repositorio remoto**
```bash
git remote -v
```

**Eliminar una rama local**
```bash
git branch -d nombre-rama
```

---

## 2. Fusionar ramas

1. Ir a la rama destino:
```bash
git checkout main
```

2. Actualizar la rama destino con el remoto:
```bash
git pull origin main
```

3. Fusionar la rama origen:
```bash
git merge develop
```

4. Resolver conflictos (si los hay):
```bash
git add <archivo>
git commit
```

5. Subir los cambios al remoto:
```bash
git push origin main
```

---

## 3. Recuperación y control de versiones

**Ver historial de commits**
```bash
git log
git log --oneline
```

**Recuperar archivos eliminados**
```bash
git checkout <id_del_commit> .
```

**Volver a un commit anterior**
```bash
git reset --hard <hash_del_commit>
```

**Volver atrás N commits**
```bash
git reset --hard HEAD~N
```

---

## 4. Limpieza y ajustes

**Eliminar archivo del repositorio (mantenerlo local)**
```bash
git rm --cached nombre_archivo
```

**Evitar que un archivo siga subiendo**
```bash
git rm --cached ruta_archivo
```

**Forzar que el repositorio remoto sea igual al local**
```bash
git push --force origin main
```

---

## 5. Subir proyecto local a repositorio remoto

**Opción 1 (paso a paso)**
```bash
git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/USUARIO/NOMBRE_REPOSITORIO.git
git push -u origin main
```

**Opción 2 (con set-upstream)**
```bash
git push --set-upstream origin main
```

---

## 6. Clonar un repositorio
```bash
git clone https://github.com/usuario/nombre-repositorio.git
cd nombre-repositorio
git status
```
