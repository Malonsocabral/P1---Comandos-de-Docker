# P1---Comandos-de-Docker

# 1. Descargar e comprobar que unha imaxe está no teu equipo
Para obtener una imagen de Docker, podemos ejecutar el siguiente comando: `docker pull {Nombre de la imagen}`, en este ejemplo, utilizaremos la imagen correspondiente a nginx.

Para verificar si unha imaxe foi descargada no tu sistema, debes utilizar o comando `docker images`.

## 2. Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome?
Para iniciar un contenedor sen asignarle un nome, usamos o comando `docker run -d nginx`.

Sí, o contenedor se executa, xa que Docker xenera automáticamente un nombre aleatorio.

Para identificar el nombre asignado, puedes utilizar o comando `docker ps -a` e verificar a columna que mostra os nomes dos contenedores, da cual suele estar ao final a derecha. Tamen podes velo en Visual Studio Code colocando o cursor sobre o contenedor.

### 3. Crea un contenedor coo nome 'u1', cómo accedes a el?

Para crear o contedor con ese nome, utilizamos o comando `docker run -d --name u1 nginx`.

E logo para acceder a el podemos empregar o comando `docker exec -it u1 /bin/bash` ou facer clic dereito sobre o contedor e seleccionar a opción **"Attach Shell"**.

#### 4. Comproba a súa ip e fai ping a google.com

Para comprobar a súa IP, utilizamos o comando `ifconfig`, e para facer ping, `ping google.com` ou `ping 8.8.8.8` que e o dns do propio google.

>[!NOTE]
>
>Debido a problemas na miña pripia experiencia, debemos tener instaladas con anterioridade certas cosas, aunque so vou deixar os comando para que sexa mias sinxelo a proxima vez,os comandos son os seguintes: `apt update`, `apt install -y iputils-ping` e `apt install -y net-tools`.

#### 5. Crea un contenedor coo nome 'bono', pódes facer ping entre os contenedores?

Primeiro de todo para crear o contenedor con ese nome utilizamos o parametro --name , é o comando seria o seguinte: `docker run -d --name bono nginx`.
>[!NOTE]
>
>Se non temos todas as ferramentas para realizar este paso, deberemos poñer os seguintes comandos `apt update`, `apt install -y iputils-ping` y `apt install -y net-tools`.

E logo para facer o propio ping utilizaremos (cabe destacar que estos comunicanse na mesma rede.):  `ping {IP del otro contenedor}`

##### 6. Se pechas as terminales, qué pasa coo contenedor?

Se pechamos todas as terminales, evidentemente pechanse todas as imaxes, isto podemolo comprobar co comando `docker ps`

7. Cánta memoria no disco duro ocupaches? usa docker para calculalo

Para ver todas as memorias que ocupa tanto a imaxe como o propio contenedor debemos poñer o comando `docker system df`. No meu caso utilizouse aproximadamente 465.2 MB _(sumando os MB da imaxe e do contenedor)_.

8. Cánta RAM ocupan os contenedores? Crea varios para calculalo

Para ver canta RAM ocupan os contenedores que acabamos de lanzar podemos utilizar o comando `docker stats`.No meu caso ocupou o _0.12%_ da RAM

9. Cómo fixeches para clonar o repositorio

Para clonar o repositorio debe usarse o comando `git clone {Dirección_do_Repositorio}`. 

>[!NOTE]
>E normalmente para saber a direcion do repositorio damoslle ao boton de code na paxina de github.

10. Cómo engades o arquivo readme2.md

Para engadir dito arquivo _(readme2.md)_ primero debemos metelo no directorio do repositorio para logo poder executar o comando `git add -A readme2.md`

11. Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md

No meu caso fagoo todo dende VS e con acceder a parte da modificacion e darlle clic derecho commit, e logo darlle un push ao repositorio, xa se sube automaticamente a web _(xa que teño a conta vinculada)_.

Agora para facelo por comandos, debemos utilizar o comando `git commit -m "Aqui pon o texto que se actualizou (é un mero comantario)"`.
E para acabar poñemos o comando `git push` para subir los cambios ao propio repositorio de github 

>[!NOTE]
>Cabe destacar que debemos ter a clave do token neste punto xa que vay pedila

12. Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote.

Entrega a tarefa enviando na resposta a dirección do teu repositorio coas respostas.

Para ver estas diferencias basta con poñer o comando `git diff origin/main`

