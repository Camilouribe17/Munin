# Configuraciones básicas y creación de dockers de prueba

## Primer paso
Debes construir un docker personalizado que incluye el servidor openssh
Usamos el siguiente comando en nuestra consola: 
               
               docker build -t server:16.04 .

## Segundo paso, despliege

Ahora debes crear una maquinas para que sea el munin master.
Usamos los siguientes comandos en nuestra consola: 

docker run -d -P --name nombre del server -p 2221:22 -p 8000:80 server:16.04


## Tercer paso, configuración de alias

Adición automática en el archivo de hosts del sistema
Usamos el siguiente comando en nuestra consola:

echo "127.0.0.1  nombre del server" | sudo tee -a /etc/hosts



# cuarto paso,Adicionar las llaves ssh</h3>
Usamos los siguientes comandos en nuestra consola: 
ssh -o StrictHostKeyChecking=no root@<nombre del server> -p 2221 -i key.private hostname


## Cuarto paso, confirmación
Realiza una prueba de conexión a la maquina que se creó recientemente.

        ssh root@nombre del server -p 2221 -i ../key.private

Si la conexión se establece, ya está listo el banco de pruebas y puedes ingresar a ansible.




