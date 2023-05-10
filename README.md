# git-course 

1. Descargar el contenido de este repositorio. (⚠️ DESCARGAR NO CLONAR) 

https://user-images.githubusercontent.com/97203617/235765971-239fec4a-5daf-476b-8be1-fa94bbdf822c.mov

2. Abrimos la carpeta que en VSCode e inicializar el repositorio. (`git init`)  y renombramos la rama princial (`git branch -M main`)
3. Creamos el primer commit  (`git add . `, `git commit -m "commit inicial" `) 

_Nota 💡 : Para ver las diferencias entre el ultimo estado conocido del repositorio en comparacion con lo que se esta trabajando actualmente_ 

4. Agregar un archivo con nuestro nombre _miNombre.md_ y vemos las diferencias (`git diff`) 
5. Agregamos el archivo al staging area (area de preparación) (`git add`) y volvemos a ver las diferencias (`git diff --staged`)
6. Creamos nuestro el siguiente commit (`git commit -m "Se agrego miNombre.md"`) 
7. Modificamos el archivo miNombre.md agregando un pequeña presentacion de nosotros: Ej: _Me llamo Georgina y estoy en al presentación de git_
8. Creamos el siguiente commit (`git commit -am "Presentacion"`) 

_Nota 💡 : el parametro -am es un forma de agrega y realizar el commit en un solo paso, esto sirve unicamente para modificaciones, no funciona en archivos nuevos_

9. Dentro del archivo de Heroes vamos a agregar uno nuevo al final del archivo y creamos el commit  (`git add heroes.md`|`git commit -m "Agregar a X heroe"`)
10. Dentro del archivo de villamos agregamos uno y creamos un commit (`git commit -am "Se agrego X villano"`)
11. Ver el historial de commit (`git log` | `git lg`) (https://gist.github.com/Klerith/0acf18bbece7923bcac55edb71b03c2b)

12. Hacer un git reset del ultimo commit (`git reset --hard <hash>`) para eliminar el commit donde se agrego un villano. 
13. Crear una rama llamada 'misiones', utilizando alguna de las distintas opciones (`git branch <nombre>`|`git checkout -b <nommbre>`|`git switch -c <nombre>`)

_Nota 💡 : Si la rama se creo con `git branch` moverse a esa rama utilizando el `git checkout` o `git switch`_

14. Agregar un archivo misiones.md y crear un commit (`git add misiones.md` | `git commit -m "agregar misiones.md"`)
15. Modificar el archivo de misiones.md, Ej: _Salvar a ciudad Gotica_, _Arreglar el batimovil_ y crear otro commit (`git commit -am "Se agregaron misiones.md"`)
16. Ver el historial del commit (`git log` | `git lg`) y comprobar que `main` se quedo atras en el historial por dos commits
17. Unir la rama misisones con main (`git checkout main`, `git merge misiones`) y eliminamos la rama misiones (`git branch -d misiones`) 
18. Modificamos el archivo de villanos y guardamos esos cambios de manera temporal (`git stash`) 
19. Modificamos el archivo de heores y guardamos esos cambios de manera temporal CON EL MENSAJE "HEROES" 	(`git stash save HEROES`) 
20. Modificamos el archivo de misiones y guardamos esos cambios temporalmente CON EL MENSAJE "MISISONES" (`git stash save MISISIONES`)
21. Vemos el listado de cambios almacenandos temporalmente (`git stash list`)
22. Aplicamos y eliminamos los cambios de villanos ( en dos pasos) 	(`git stash apply <id>` | `git drop <id>`) 
23. Aplicamos y eliminamos los cambios de herores ( en 1 paso) (`git stash pop` | `git stash pop <id>`) 
24. Vemos el listado de cambios almacenandos temporalmente y los eliminamos (`git stash list` `git stash clear`)
25. Creamos una nueva rama "misiones-V2" SOLO LA CREAMOS (`git branch misiones-V2`)
26. Modificamos le archivo heroes.md,  creamos un nuevo commit (`git commit -am "agregamos a x en heores.md"`) y vemos el historial de commig (`git log`|	`git lg`)
27. Nos movemos a la rama que creamos anteriormente (`git checkout misiones-V2` | `git switch misiones-V2`)

_Nota 💡: Se puede observar que la rama main tiene un commit extra que no esta dentro de la rama  misiones-V2_ 

28. Actualizamos la rama misiones-V2. (`git rebase misisones-V2`) y vemos el historial de commits (`git log` | `git lg`) 

_Nota 💡: Si hubieramos tenido cambios (commits) que solo estuvieran en la rama misiones-rebase esos cambios se hubieran ido hasta el final del listado de commit_ 

29. Modificamos el archivo de misiones y creamos un commit (`git add misiones.md` ` git commit -m "agregamos a x en misiones.md"`)
30. Modificamos el archivo de villanos y creamos un commit (`git add villanos.md`  `git commit -m "agregamos a x en villanos.md"`)

_Escenario 💡: por alguna extraña razon necesitamos que los villanos que agregamos (30) esten en la rama principal, pero auno no tenemos que agregar las nuevs misiones, entonces tenemos que mover el (los) commit(s) en donde agregamos a los villamos a la rama principal_

31. Nos movemos a la rama princial (`git checkout main`) 
32. Vemos el historial de commits (`git log` | `git lg`) y copiamos el hash/id del commit en donde agremos a los villamos 
32. Movemos/Copiamos el commit a al rama principal (`git cherry-pick <id>`) 

_Extra ✚ : Podemos movernos a la rama misiones-V2 y eliminar el ultimo commit (donde agreamos a los villanos (30)) con in git reset --hard (`git reset --hard <id>`)_

33. Vamos a crear un Repositorio en GitHub (https://docs.github.com/es/get-started/quickstart/create-a-repo#create-a-repository)
<img width="816" alt="Screen Shot 2023-05-02 at 12 59 13" src="https://user-images.githubusercontent.com/97203617/235760455-32efb123-118b-414b-a1d0-3755f299d800.png">

34. Agregamos un repositorio remoto al repo local en el que hemos estado trabajando (`git remote add origin <url>`)
<img width="1269" alt="Screen Shot 2023-05-02 at 12 59 26" src="https://user-images.githubusercontent.com/97203617/235760486-e018f8b0-52b7-46e9-b08b-47c8d0142b60.png">

35. Verificamos que se agrego de manera correcta (`git remote -v`) 
36. Subimos los cambios del repo local al repo remoto (`git push -u origin main`)
37. Recargamos la pagina de nuestro repositorio remoto. 

# Listo! :tada:





