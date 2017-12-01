## Configuracion de Ansible
Se instalaran  y configuraran estos  2 servicios : 
<ul>
  <li>Apache</li>
  <li>Munin</li>
  
</ul>

<h3>Primer paso, instalación del servidor web</h3>
## - Instalamos el servidor web en el localhost de nuestra maquina
ansible-playbook -i hosts install_apache.yml


## - Instalamos Munin en el localhost para que actue como nodo
ansible-playbook -i hosts install_munin_node.yml


## - Instalamos Munin en el munin_master_web_server
ansible-playbook -i hosts install_munin_master.yml
