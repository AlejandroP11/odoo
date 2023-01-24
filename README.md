# odoo

# Docker-Compose 

Para generar el docker-compose, primero debemos buscar la imagen oficial de Odoo en DockerHub, donde encontraremos el código más simple y sin fallos para generarlo. Aquí podremos encontrar que para crear un docker-compose para la imagen de Odoo debemos prestar mucha atención en **depends on:** que es donde pondremos el nombre que le daremos al contenedor de la base de datos. Además de esto añadiremos el puerto que vamos a usar, este caso el 8069, y el nombre del contenedor.
Para la imagen de Postgres lo más importante a tener en cuenta es el puerto que utilizaremos, esta vez el 5032, ya que por este puerto nos contectaremos a la misma, también usaremos su volumen para guardar los datos y, próximamente, crear el proyecto en PyCharm.
  
  ![Screenshot_20230124_060324](https://user-images.githubusercontent.com/91608906/214359078-72f3ca9f-3703-45d1-98f3-43e1f8bf286f.png)

Con este docker-compose solo nos quedaría lanzarlo con el comando **docker-compose up** y esperar a que se inicien nuestro servicios.

#PyCharm 
Una vez iniciados abriremos un nuevo proyecto en PyCharm, para esto solo debemos abrir la carpeta en la que guardamos el volumen de nuestra base de datos.

#Docker con PyCharm
Para utilizar Docker primero debemos descargarlo como pluggin, pestaña que podremos encontrar dentro de la configuaración del proyecto. Una vez lo hayamos instalado, debemos ir a la pestaña de **Build, Execution, Deployment** y seleccionar Docker.

  ![Screenshot_20230124_052249](https://user-images.githubusercontent.com/91608906/214361394-02981614-ae0a-47c8-b309-6883faf4255c.png)

Con esto podemos encontrar Docker en la pestaña de servicios en la parte inferior de nuestro IDE, desde aquí podemos controlar todos nuestro contenedores.

![Screenshot_20230124_052419](https://user-images.githubusercontent.com/91608906/214361862-7d4c7a3e-f137-4273-9664-9ad1deafd4cd.png)

#Base de Datos
Con la base de datos tendremos que volver a utilizar un pluggin, debido a que, en mi caso por lo menos, PyCharm no cuenta con una pestaña predeterminada para estas. Volvemos a la pestaña de pluggins y encontraremos este en concreto: 

  ![Screenshot_20230124_052852](https://user-images.githubusercontent.com/91608906/214362257-f54ff259-5f20-4aa6-80a5-58530372eee9.png)

Una vez lo instalemos tendremos en la parte izquierda de nuestro IDE una pestaña nueva que dice **Data Base Server**, presionaremos esta y encontraremos un menú parecido al que podemos encontrar en otros IDEs, es cuestión de rellenar los datos que esta nos indica y probar la conexión. Si hicimos todo bien, nos debería salir un mensaje mostrando que la conexión se realizó con exito y la pestaña **Data Base Server** se verá así: 

  ![Screenshot_20230124_053832](https://user-images.githubusercontent.com/91608906/214363079-91e64895-f467-4332-854f-b8288b5f4489.png)

Así podremos manejar nuestros contenedores, la base de datos y todos los datos de la misma dentro de PyCharm. 
