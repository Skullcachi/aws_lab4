# aws_lab4
Laboratorio 4 de aws
Este laboratorio contiene una aplicación desarrollada en node.js que se ejecuta en el puerto 3000
Para poder correr una instancia con este proyecto es necesario instalar las siguientes dependencias dentro de la instancia:
Instalar Node: 
  Correr el siguiente comando en CLI: curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
Instalar Git:
  correr el siguiente comando en CLI: sudo yum install git
  
Crear una carpeta con mk nombredelacarpeta
cd nombredelacarpeta
Clonar este repositorio
Navegar a aws_lab4/movies/
  Correr el siguiente comando en CLI: node src/app.js
  
 La aplicacion deberia de iniciarse en el puerto 3000
 
 Para acceder a la aplicación hay que copiar el DNS publico de la instancia y agregarle :3000 al final y ya se puede acceded a la aplicacion.


Procedimiento para realizar el laboratorio
1. Crear una instancia en EC2
2. Crear un Segurity Group que permitan conexiones de protocolo http puerto 80
3. Crear un Load Balancer, con su respectivo listener al puerto:3000 (puerto de node.js donde esta la app ejecutandose) y configurar su health check para que haga ping cada 5 segundos para comprobar que haya conexión.
4. Crear un AutoScaling group con 2 instancias default, seteandole que se accionen nuevas instancias cuando el uso de la instancia principal sobrepase los 30%. Adicional, 2 alarma para cuando se activen las instancias se envien correos, de igual manera para cuando las instancias de desactiven por porcentaje de usuario.
