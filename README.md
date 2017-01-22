# redes
En este ejercicio vamos a configurar distintas redes, de las cuales algunas tendras servidor DNS, servidores DHCP, puntos de acceso,etc.. Esto es lo que hemos realizado en el cisco packet tracer:

-En general tenemos que asignar una ip a cada router con una puerta de enlace y mascaras validas, para este ejercicio necesitamos 5 routers, tambien hay que destacar que la ip y mascara se le asigna en el FastEthernet, a los routers hay que añadirle el modulo WIC-1T para que podamos conectarnos de un router a otro, en cada router tambien tenemos que asignar en el apartado Serial y poner la ip y mascara que tiene el router al que esta conectado para que luego exista una conexion entre varias redes, claramente no pueden repetirse ninguna ip ni fallos en la puerta de enlace ya que en ese caso no podriamos hacer que la conexion entre varias redes funcione completamente.

-En el primer router nos piden que hagamos 3 subredes, y que solo una de ellas pueda comunicarse con otras redes, despues de configurar el router como hemos explicado antes, usaremos un swich al cual van a estar conectados 12 ordenadores, conectamos los pc al swich por FastEthernet, le asignamos una ip estatica que este dentro del rango de la subred que nos pedia el ejercicio, y una puerta de enlace valida.

-En el segundo router aparte de lo usado anteriormente nos hara falta un servidor en el cual configuraremos para que nos asigne ip a los ordenadores ya que estara con DHCP, primero tenemos que darle una ip fija,mascara y puerta de enlace a el servidor. En este caso vamos a usar como servidor DNS este servidor asique nos iremos al apartado DNS, ponemos la direccion de la puerta de enlace, la ip del servidor en servidor dns y podemos elegir desde que rango queremos que nos asigne ip el servidor a los ordenadores, despues solo nos queda conectar el servidor al switch y este que este conectado a los ordenadores, y estos a su vez que esten configurados para estar con la configuracion DHCP. En el servidor DNS tambien cambiaremos algunos datos, en HTTP borraremos todos los datos menos el index.html en el que insertaremos estas lineas:

<html>
<head>
</head>
<body>
	<p align="center">
		<h1>Albacete</h1>
		<img src="albacete.jpg"/>
	<p/>
<body/>
<html/>

Que nos serviran para visualizar una foto de cada lugar que nos ha pedido el ejercicio escribiendo la direccion web del mismo,por ejemplo www.albacete.es Esto tenemos que hacerlo en cada servidor solo que cambiando los datos por los de otro lugar como dilar y cambiando la foto por una del sitio dicho.
En el apartado DNS apuntaremos las direcciones web de las otras paginas que nos pide el ejercicio.

-En el tercer router tenemos que configurar un servidor para que funcione para 4 ordenadores por DHCP asi que seguiremos los pasos que hicimos para ello en el segundo router. Con la unica diferencia de que tengan una red distinta a la anterior y no se repitan ip o que no existan las mismas.

-En el 4to router podemos seguir los pasos de router anteriores pero la diferencia esta vez es que necesitamos un punto de acceso, los ordenadores que esten conectados a ese punto de acceso estaran conectados por DHCP y el servidor estara dedicado unicamente para ellos ya que el se encargara de asignar las ip, los ordenadores que estan conectados al punto de acceso han usado un modulo que les permita detectar redes inalambricas y asi poder conectarse, los demas ordenadores que estan directamente conectados al switch tienen una ip fija.

-En el ultimo router estaran 4 ordenadores conectados al switch con una ip fija asi que podemos seguir pasos anteriores.

