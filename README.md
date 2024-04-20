#STORM VIEWER

En este proyecto, se realizó una aplicación que permitirá a los usuarios desplazarse por una lista de imágenes y luego seleccionar una para mostrarla en pantalla.

# Listado de imágenes con FileManager

![](https://github.com/adrian220699/Storm-viewer/blob/main/img_01.png?raw=true)


* La línea let fm = FileManager.defaultdeclara una constante llamada fmy le asigna el valor devuelto por FileManager.default. Este es un tipo de datos que nos permite trabajar con el sistema de archivos y, en nuestro caso, lo usaremos para buscar archivos.

* La línea let path = Bundle.main.resourcePath!declara una llamada constante pathque se establece en la ruta de recursos del paquete de nuestra aplicación. Recuerde, un paquete es un directorio que contiene nuestro programa compilado y todos nuestros activos. Entonces, esta línea dice: "dime dónde puedo encontrar todas esas imágenes que agregué a mi aplicación".

* La línea let items = try! fm.contentsOfDirectory(atPath: path)declara una tercera constante llamada itemsque se establece en el contenido del directorio en una ruta. ¿Qué camino? Bueno, el que fue devuelto por la línea anterior. Como puede ver, los nombres largos de los métodos de Apple realmente hacen que su código sea bastante autodescriptivo. La itemsconstante será una matriz de cadenas que contienen nombres de archivos.

* La línea for item in items {inicia un bucle que se ejecutará una vez por cada elemento que encontremos en el paquete de la aplicación. Recuerde: la línea tiene una llave de apertura al final, que indica el inicio de un nuevo bloque de código, y hay una llave de cierre coincidente cuatro líneas debajo. Todo lo que esté dentro de esas llaves se ejecutará cada vez que se realice el ciclo.

* La línea if item.hasPrefix("nssl") {es la primera línea dentro de nuestro bucle. En este punto, tendremos el primer nombre de archivo listo para trabajar y se llamará item. Para decidir si es uno que nos interesa o no, usamos el hasPrefix()método: toma un parámetro (el prefijo a buscar) y devuelve verdadero o falso. Ese "si" al principio significa que esta línea es una declaración condicional: si el elemento tiene el prefijo "nssl", entonces... así es, otra llave de apertura para marcar otro nuevo bloque de código. Esta vez, el código se ejecutará solo si hasPrefix()devuelve verdadero.

* Finalmente, la línea // this is a picture to load!es un comentario: si llegamos aquí, itemcontiene el nombre de una imagen para cargar desde nuestro paquete, por lo que debemos almacenarla en algún lugar.

Creamos una vartiable de la siguiente forma para contener las imagenes dentro de un arreglo.

`var pictures = [String]()`

Posteriormente almacenamos las imagenes dentro del arreglo.

`pictures.append(item)`


# Diseñando interfaz


![](https://github.com/adrian220699/Storm-viewer/blob/main/img_02.png?raw=true)



#Construyendo una pantalla de detalles


![](https://github.com/adrian220699/Storm-viewer/blob/main/img_03.png?raw=true)



#Cargando imágenes con UIImage


![](https://github.com/adrian220699/Storm-viewer/blob/main/img_04.png?raw=true)


#Ajustes finales: hidesBarsOnTap y títulos grandes


![](https://github.com/adrian220699/Storm-viewer/blob/main/img_05.png?raw=true)


