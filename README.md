# EstacionProcesos

A continuación voy a resumir el funcionamiento general de la estación, asi como el de cada módulo por separado, para hacer más facil la comprensión del código.
Dentro del proyecto de Step7 está documentado y comentado cada paso con más exactitud, los direccionamientos de actuadores y sensores vienen especificados en el pdf
adjunto.

- Funcionamiento general:
    
    La función de esta estación consiste en detectar una pieza solicitada mediante una tabla, y realizarle el tratamiento adecuado en función del tipo de pieza (Métalica,
    plástico roja o plástico negra), por último expulsará la pieza y borrará el pedido de la cola.
    

- Función de cada módulo:

  1- El primer módulo se encarga simplemetne de detectar una nueva entrada en la lista de pedidos e introducir, mediante un pistón, una pieza de una cola de piezas 
     aleatorias.
  
  2- En el segundo módulo es donde comprobamos mediante senosres que tipo de pieza se ha introducido. En caso de que en la lista de pedidos haya una pieza de este 
     tipo (si pedimos 6 piezas comprobará toda la lista, no solo la última entrada) la subirá mediatne un  pistón para darle paso a la siguiente estación, sin embargo
     si en la lista de pedidos no hay ninguna pieza de este tipo, la expulsaremos de la estación mediante un pistón.
     
  3- El tercer módulo se trata de un plato giratorio mediante el cual realizaremos un taladro en nuestras piezas. (Para controlar la posición de nuestra pieza respecto
     a las distintas herramientas de este módulo usaremos el desplazamiento de bits)
     
  4- Este módulo se encarga de transportar las piezas del módulo 3 al 5 mediante un gancho.
  
  5- Por último la quinta estacón se encargará de introducir un émbolo en el taladro que le hemos realizado a las piezas, expulsar la pieza y borrarla de la lista de
     pedidos. El embolo será ancho para las piezas negras y más estrecho para rojas y metálicas.
