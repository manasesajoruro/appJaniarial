# header
- falta centrar el logo
- que reduzca su tamaño
# menu
- centrar el menu
- transicion de la derecha a la izq
 
# 1. verificar usuario y correo
git config user.name
git config user.email
# para cambiar de usuario
git config user.name "tunombre"
git config user.email "tucorreo@gmail.com"

# clonar repositorio remoto
git clone git@manases:usuario/su-repo.git
git remote -v | verifica el repositorio remoto

# subir por primera vez
# Crear rama main (si no existe)
git branch -M main
# Subir por primera vez
git push -u origin main

# subida normal
git status     para ver los cambios
git add .       para añadir los cambio
git commit -m "comentario..."   
git push -u origin main     Con esto lo subo 