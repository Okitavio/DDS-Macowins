# DDS-Macowins
Resolución de ejercicio de Diseño de Sistemas de UTN.BA

De la lectura de la consigna identifiqué los siguientes tres requerimientos:
1) Saber el precio de venta de una prenda y su tipo
2) Saber el precio total de una venta
3) Saber las ganancias de un determinado día

Planteo como una posible solución tener una clase Prenda que tenga un atributo Estado que apunte a una de las tres clases asociadas: Nueva, Promoción y Liquidación. De esta manera, el método calcularPrecio de la clase Prenda se puede redefinir si fuese necesario para obtener el precio de promoción o liquidación. La responsabilidad de calcular su precio recae sobre la Prenda (para cumplir con el requerimiento 1).

Una alternativa que consideré pero luego descarté fue la de tener a Prenda como una clase abstracta y que las clases concretas fueran Saco, Pantalón y Camisa. Esta configuración puede que se acerque más al modelo real pero no me pareció prudente trasladarlo al modelo de objetos dado que los distintos tipos de prendas no presentan un comportamiento diferente según su tipo.

Por otro lado tenemos la clase Venta que tiene una lista de prendas, la fecha en que tuvo lugar y el número de cuotas que elige el cliente para abonar. De esta forma tiene todo lo necesario para calcular el precio total de la venta y cumplir con el requerimiento 2.

Por último, decidí incluir una clase Macowins que representaría al local físico al que ayuda a administra sus ventas. Esta clase tiene la responsabilidad de calcular las ganancias de un día en específico (requerimiento 3) y toda funcionalidad que se necesite agregar más adelante.
