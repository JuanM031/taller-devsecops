# Taller DevSecOps

DevSecOps es una práctica que integra seguridad dentro del ciclo de vida del desarrollo de software, automatizando controles de seguridad dentro del proceso DevOps.

# Evidencia redactada – Actividad 2
Durante la actividad se creó una estructura de proyecto local utilizando la herramienta Git para el control de versiones. Inicialmente se creó la carpeta taller-devsecops, dentro de la cual se inicializó un repositorio mediante el comando git init. Posteriormente se creó el archivo README.md, en el que se incluyó una breve descripción sobre el concepto de DevSecOps.
Luego se realizó el primer snapshot del proyecto agregando el archivo al área de preparación con git add README.md y posteriormente creando el primer commit con el comando git commit, registrando así el estado inicial del proyecto en el repositorio local.
Posteriormente se creó un repositorio privado en la plataforma GitHub con el nombre taller-devsecops, el cual funcionará como repositorio remoto. Después se cambió el nombre de la rama principal a main y se configuró la conexión entre el repositorio local y el remoto utilizando el comando git remote add origin.
Finalmente, se realizó la sincronización del proyecto mediante el comando git push -u origin main, logrando subir el código al repositorio remoto y estableciendo la rama main local para rastrear la rama origin/main en GitHub. Con esto se completó correctamente el ciclo de vida básico desde un entorno local hacia un repositorio en la nube.
Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIEZSZQDdS58PuMNam0TiTva3g8RxMTLIZR2zeQVdb74N juan-jose13@hotmail.es

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ^C

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ssh -T git@github.com
The authenticity of host 'github.com (140.82.113.4)' can't be established.
ED25519 key fingerprint is: SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])?
Host key verification failed.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ssh -T git@github.com
The authenticity of host 'github.com (140.82.113.4)' can't be established.
ED25519 key fingerprint is: SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? YES
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
git@github.com: Permission denied (publickey).

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ eval "$(ssh-agent -s)"
bash: Mesa/.ssh/agent/s.NzcG0bwIHi.agent.Cwd49iwuNM: No such file or directory
Agent pid 942

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ssh-add ~/.ssh/id_ed25519
Could not open a connection to your authentication agent.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$
eval $(ssh-agent)
bash: Mesa/.ssh/agent/s.NzcG0bwIHi.agent.zTr8jHW0DV: No such file or directory
Agent pid 958

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ssh-add ~/.ssh/id_ed25519
Could not open a connection to your authentication agent.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ssh -T git@github.com
Hi JuanM031! You've successfully authenticated, but GitHub does not provide shell access.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ git remote -v
origin  https://github.com/JuanM031/taller-devsecops.git (fetch)
origin  https://github.com/JuanM031/taller-devsecops.git (push)

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ git remote set-url origin git@github.com:JuanM031/taller-devsecops.git

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ git remote -v
origin  git@github.com:JuanM031/taller-devsecops.git (fetch)
origin  git@github.com:JuanM031/taller-devsecops.git (push)

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ git push
Everything up-to-date

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ ^[[200~mkdir taller-devsecops
bash: $'\E[200~mkdir': command not found

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ cd taller-devsecops
bash: cd: taller-devsecops: No such file or directory

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ git initmkdir taller-devsecops
cd taller-devsecops
git init
git: 'initmkdir' is not a git command. See 'git --help'.
bash: cd: taller-devsecops: No such file or directory
Reinitialized existing Git repository in C:/Users/Juan Mesa/taller-devsecops/taller-devsecops/.git/

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops (main)
$ mkdir taller-devsecops
cd taller-devsecops
git init
Initialized empty Git repository in C:/Users/Juan Mesa/taller-devsecops/taller-devsecops/taller-devsecops/.git/

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (master)
$ echo "# Taller DevSecOps
DevSecOps es una práctica que integra la seguridad dentro del ciclo de vida del desarrollo de software, automatizando controles de seguridad en cada etapa del proceso DevOps." > README.md

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (master)
$ git add README.md
git commit -m "Primer commit - README DevSecOps"
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it
[master (root-commit) 3f4fc3b] Primer commit - README DevSecOps
 1 file changed, 2 insertions(+)
 create mode 100644 README.md

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (master)
$ git branch -M main

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git remote -v

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git remote -v

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git remote -v

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git remote add origin git@github.com:JuanM031/taller-devsecops.git

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git remote -v
origin  git@github.com:JuanM031/taller-devsecops.git (fetch)
origin  git@github.com:JuanM031/taller-devsecops.git (push)

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git push -u origin main
To github.com:JuanM031/taller-devsecops.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:JuanM031/taller-devsecops.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git pull origin main --allow-unrelated-histories
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 7 (delta 1), reused 7 (delta 1), pack-reused 0 (from 0)
Unpacking objects: 100% (7/7), 695 bytes | 8.00 KiB/s, done.
From github.com:JuanM031/taller-devsecops
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
Auto-merging README.md
CONFLICT (add/add): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main|MERGING)
$ git push -u origin main
To github.com:JuanM031/taller-devsecops.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:JuanM031/taller-devsecops.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main|MERGING)
$ code README.md

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main|MERGING)
$ git add README.md
git commit -m "Resolución de conflicto README"
[main 9e36ff5] Resolución de conflicto README

Juan Mesa@PRUEBAINCATECJM MINGW64 ~/taller-devsecops/taller-devsecops/taller-devsecops (main)
$ git push -u origin main
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 2 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 633 bytes | 211.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To github.com:JuanM031/taller-devsecops.git
   9f6b4d5..9e36ff5  main -> main
branch 'main' set up to track 'origin/main'.






 # Evidencia – Actividad 3: Autenticación segura con SSH

 Con el fin de evitar el uso de contraseñas en texto plano al interactuar con repositorios remotos, se implementó un mecanismo de autenticación segura mediante llaves SSH entre el equipo local y la plataforma GitHub utilizando el sistema de control de versiones Git.
Inicialmente se generó un par de llaves criptográficas usando el algoritmo Ed25519 mediante el siguiente comando:
 
Este proceso generó dos archivos dentro del directorio .ssh del usuario:
•	id_ed25519 → llave privada (permanece segura en el equipo local)
•	id_ed25519.pub → llave pública (se comparte con GitHub)
Posteriormente, la llave pública fue copiada y registrada en la configuración de seguridad de la cuenta de GitHub dentro de la sección SSH Keys, permitiendo que la plataforma reconozca el equipo autorizado.
Para validar la configuración se ejecutó el siguiente comando:
 
Esto confirmó que la conexión segura fue establecida correctamente. Finalmente se cambió la URL del repositorio remoto para utilizar el protocolo SSH y se realizó un git push, logrando subir los cambios al repositorio sin necesidad de ingresar usuario ni contraseña.
De esta forma se implementó correctamente un método de autenticación seguro basado en criptografía asimétrica, alineado con las buenas prácticas de seguridad en entornos DevSecOps.

Llave publica:
 

# Preguntas Orientadoras (Análisis DevSecOps)

1. Trazabilidad: ¿Por qué es un riesgo de seguridad dejar la configuración de user.name y user.email vacía o utilizar datos genéricos en un entorno empresarial?
Dejar el user.name y user.email vacíos o usar datos genéricos es un riesgo porque no se puede saber quién hizo los cambios en el código. En una empresa es importante identificar qué persona realizó cada modificación para poder hacer seguimiento, corregir errores o investigar problemas de seguridad.

2. Cifrado Asimétrico: En el caso de usar SSH, ¿cuál es la diferencia funcional entre la llave privada y la pública? ¿Qué pasaría si un tercero obtiene acceso a tu llave privada?
La llave pública se sube a plataformas como GitHub para identificar al usuario, mientras que la llave privada se guarda en el computador y sirve para demostrar que eres el dueño de esa cuenta. Si alguien obtiene la llave privada, podría acceder al repositorio como si fuera el usuario legítimo.

3. Principio de Mínimo Privilegio: Si decides usar un Token de Acceso Personal (PAT), ¿qué riesgos conlleva asignarle permisos de "Administrador" (Full Control) en lugar de solo permisos de "Lectura/Escritura"?
Si a un token se le dan permisos de administrador, alguien que lo robe podría tener control total del repositorio. Por eso es mejor darle solo los permisos necesarios, como lectura y escritura, para reducir los riesgos.

4. Higiene del Repositorio: ¿Para qué sirve el archivo .gitignore desde una perspectiva de seguridad? (Menciona al menos dos tipos de archivos que nunca deberían subirse al repositorio remoto).
El archivo .gitignore sirve para evitar que ciertos archivos se suban al repositorio. Esto ayuda a proteger información sensible. Por ejemplo, no se deberían subir archivos con contraseñas o claves, como .env, ni llaves privadas de acceso.

5. Exposición de Secretos: Si accidentalmente subes una llave de API o una contraseña al repositorio en GitHub, ¿es suficiente con borrarla y hacer un nuevo commit? Justifica tu respuesta.
Si se sube por error una contraseña o una llave de API a un repositorio en GitHub, no basta con borrarla y hacer otro commit. Esto se debe a que Git guarda el historial de cambios y la información todavía podría verse en versiones anteriores. Por eso también se debe cambiar o cancelar esa credencial.
