Insatalacion de pandora en un sistema debian, incluyendo consola, servidor y agente.

Para empezar descargamos los paquetes desde el siguiente enlace: Enlace (https://pandorafms.org/en/features/free-download-monitoring-software/)

Luego instalamos los paquetes con los siguientes comandos <br>
  <code>### XXX es la version del paquete.  </code><br>
  <code># dpkg -i pandorafms.console_XXX.deb  </code><br>
  <code># apt-get -f install  </code><br>
  <code># dpkg -i pandorafms.server_XXX.deb </code><br>
  <code># apt-get -f install </code><br>
  <code># dpkg -i pandorafms.agent_XXX.deb  </code><br>
  <code># apt-get -f install  </code><br>

Ahora hay que instalar el servidor de la base de datos MySQL <br><br>
  <code># apt-get install mysql-server </code><br><br>

Despues se modifica el fichero “etc/apache2/sites-enabled/000-default.conf” para hacer de la consola la pagina de inicio
cambiando la linea “DocumentRoot /var/www/pandora_console”. Y se reinicia el servicio de apache con el siguiente comando:
  <br><br>
  <code># /etc/init.d/apache2 restart </code><br><br>