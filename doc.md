# header
- falta centrar el logo
- que reduzca su tamaño
# menu
- centrar el menu
- transicion de la derecha a la izq
 
 # 🚀 Subir Proyecto Existente a GitHub

## **PASO 1: Crear repositorio en GitHub**

1. Ve a [github.com](https://github.com)
2. Click en **"New repository"** (botón verde)
3. **Nombre del repositorio:** Usa el mismo nombre de tu carpeta de proyecto
4. **⚠️ IMPORTANTE:** NO marques "Add a README file"
5. **⚠️ IMPORTANTE:** NO agregues .gitignore ni licencia
6. Click **"Create repository"**

## **PASO 2: Navegar a tu proyecto local**

```bash
# Ir a la carpeta de tu proyecto
cd /ruta/a/tu/proyecto

# Verificar que estás en la carpeta correcta
ls -la
```

## **PASO 3: Inicializar Git (si no lo has hecho)**

```bash
# Verificar si ya tienes git inicializado
ls -la | grep .git

# Si NO aparece .git, inicializar:
git init

# Si ya tienes .git, saltar este paso
```

## **PASO 4: Configurar usuario para este proyecto**

```bash
# CRÍTICO: Configurar TU usuario para este proyecto
git config user.name "Manases Ajoruro"
git config user.email "manasesajoruro@gmail.com"

# Verificar que quedó bien
git config user.name
git config user.email
```

## **PASO 5: Crear .gitignore (muy importante)**

```bash
# Crear archivo .gitignore
nano .gitignore
```

**Contenido básico según tu proyecto:**

```
# Dependencias
node_modules/
npm-debug.log*

# Variables de entorno
.env
.env.local

# Archivos del sistema
.DS_Store
Thumbs.db

# Archivos temporales
*.log
*.tmp
temp/

# Builds
dist/
build/
out/

# IDEs
.vscode/
.idea/
*.swp
*.swo
```

Guarda con `Ctrl+X`, luego `Y`, luego `Enter`.

## **PASO 6: Agregar archivos al repositorio**

```bash
# Ver qué archivos tienes
git status

# OPCIÓN A: Agregar archivos específicos (RECOMENDADO)
git add src/
git add index.html
git add package.json
# ... agregar los archivos que SÍ quieres subir

# OPCIÓN B: Agregar todo (CUIDADO - revisar primero)
git add .

# Verificar qué vas a subir
git status
```

## **PASO 7: Hacer primer commit**

```bash
# Primer commit
git commit -m "Initial commit - agregar proyecto base"

# Verificar que el commit se hizo
git log --oneline
```

## **PASO 8: Conectar con GitHub**

```bash
# Agregar repositorio remoto (reemplaza TU-USUARIO y NOMBRE-REPO)
git remote add origin git@manases:TU-USUARIO/NOMBRE-REPO.git

# Verificar que se agregó correctamente
git remote -v
```

**Debe mostrar algo como:**
```
origin  git@manases:tu-usuario/nombre-proyecto.git (fetch)
origin  git@manases:tu-usuario/nombre-proyecto.git (push)
```

## **PASO 9: Subir a GitHub**

```bash
# Crear rama main (si no existe)
git branch -M main

# Subir por primera vez
git push -u origin main
```

## **VERIFICACIÓN FINAL**

1. **Ir a tu repositorio en GitHub** - deberías ver todos tus archivos
2. **Verificar commits** - debe aparecer tu nombre como autor
3. **Probar clonación** en otra carpeta para verificar

## **COMANDOS COMPLETOS (EJEMPLO)**

Ejemplo para un proyecto llamado "mi-app":

```bash
# 1. Ir al proyecto
cd /ruta/a/mi-app

# 2. Configurar usuario
git config user.name "Manases Ajoruro"
git config user.email "manasesajoruro@gmail.com"

# 3. Inicializar git (si es necesario)
git init

# 4. Crear .gitignore
echo "node_modules/" > .gitignore
echo ".env" >> .gitignore

# 5. Agregar archivos
git add .

# 6. Primer commit
git commit -m "Initial commit"

# 7. Conectar con GitHub
git remote add origin git@manases:manases-usuario/mi-app.git

# 8. Subir
git branch -M main
git push -u origin main
```

## **⚠️ ERRORES COMUNES**

1. **Usuario incorrecto** - Verificar `git config user.email`
2. **URL incorrecta** - Debe usar `git@manases:` no `git@github.com:`
3. **Archivos sensibles** - Revisar que .gitignore esté bien
4. **Repositorio no vacío** - Si marcaste README en GitHub, tendrás conflictos

## **SI HAY ERRORES**

```bash
# Error de autenticación
ssh -T git@manases

# Error de URL remota
git remote set-url origin git@manases:usuario/repo.git

# Conflictos por README
git pull origin main --allow-unrelated-histories
```

---

**¿Cuál es el nombre de tu proyecto y dónde está ubicado?** Te ayudo con los comandos específicos.