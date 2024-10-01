# P1---Comandos-de-Docker

1. Descargar e comprobar que unha imaxe está no teu equipo
Para obtener una imagen de Docker, podemos ejecutar el siguiente comando: `docker pull {Nombre de la imagen}`, en este ejemplo, utilizaremos la imagen correspondiente a nginx.

Para verificar si unha imaxe foi descargada no tu sistema, debes utilizar o comando `docker images`.

2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?
Para iniciar un contenedor sen asignarle un nome, usamos o comando `docker run -d nginx`.

Sí, o contenedor se executa, xa que Docker xenera automáticamente un nombre aleatorio.

Para identificar el nombre asignado, puedes utilizar o comando `docker ps -a` e verificar a columna que mostra os nomes dos contenedores, da cual suele estar ao final a derecha. Tamen podes velo en Visual Studio Code colocando o cursor sobre o contenedor.

3. Crea un contenedor coo nome 'u1', cómo accedes a el?

Para crear o contedor con ese nome, utilizamos o comando `docker run -d --name u1 nginx`.

E logo para acceder a el podemos empregar o comando `docker exec -it u1 /bin/bash` ou facer clic dereito sobre o contedor e seleccionar a opción *"Attach Shell"*.

4. Comproba a súa ip e fai ping a google.com

Para comprobar a súa IP, utilizamos o comando `ifconfig`, e para facer ping, `ping google.com` ou `ping 8.8.8.8` que e o dns do propio google.

Debido a problemas na miña pripia experiencia, debemos tener instaladas con anterioridade certas cosas, aunque so vou deixar os comando para que sexa mias sinxelo a proxima vez,os comandos son os seguintes: `apt update`, `apt install -y iputils-ping` e `apt install -y net-tools`.

5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?
>[!NOTE]
>
>Prueba de nota

6. Se pechas as terminales, qué pasa coo contenedor?

7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

9. Cómo fixeches para clonar o repositorio

10. Cómo engades o arquivo readme2.md

11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.

Entrega a tarefa enviando na resposta a dirección do teu repositorio coas respostas.