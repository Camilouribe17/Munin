# Cofiguración de Ansible


Se instalaran  y configuraran estos  2 servicios : 
<ul>
  <li>Apache</li>
  <li>Munin</li>
  
</ul>

<h3>Primer paso, instalación del servidor web</h3>


### -instalamos el servidor web en el localhost de nuestra maquina

utilizamos el sguiente comando en nuestra consola : 

ansible-playbook -i hosts install_apache.yml


<h2>Instalacion de Munin</h2>

### -Intalamos Munin en el localhost para que actue como nodo

utilizamos el sguiente comando en nuestra consola : 

ansible-playbook -i hosts install_munin_node.yml


### -Intalamos Munin en el munin_master_web_server

utilizamos el sguiente comando en nuestra consola : 

ansible-playbook -i hosts install_munin_master.yml



