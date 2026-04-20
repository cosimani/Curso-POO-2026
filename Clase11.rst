Clase 11 - 20 de abril de 2026
==============================





Registro en video de algunos temas de la clase de hoy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`Login con QtDesigner 2026 <https://youtu.be/rcNz_rKD7PQ>`_

`Array como parámetro QTextEdit Preprocesador Guardián 2025 <https://youtu.be/RThbIuZvrJQ>`_

`Login en empty project 2025 <https://youtu.be/Gdo6NcdOuPo>`_

`Login con QtDesigner 2025 <https://youtu.be/9Z208vj-jCw>`_

`Sutileza con punteros - octal - arrays como parámetros 2021 <https://www.youtube.com/watch?v=XQOBvBVkffM>`_

`QNetworkAccessManager y colocar imagen en login 2023 <https://youtu.be/PFSWwS-RHyI>`_

`Login con imagen generando código con el chat 2024 <https://youtu.be/vVbO58KlNO8>`_

`Array como parámetros - QTextEdit y aritmética de punteros 2023 <https://youtu.be/FzbxG3KJkdE>`_

`QGroupBox - QString number 2021 <https://www.youtube.com/watch?v=c7_axxXbphU>`_

`Preprocesador y guardían de inclusión múltiple 2023 <https://youtu.be/75RIKDem8NI>`_




-----------------------------------





Array como parámetro en funciones
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block::

	#include <iostream>
	using namespace std;

	void funcion( int miArray[] );
	// Le estamos pasando un puntero al primer elemento del array.

	int main()  {
	    int miA[ 5 ] = { 0, 1, 2, 3, 4 };

	    funcion( miA );

	    cout << miA[ 0 ] << miA[ 1 ] << miA[ 2 ] << miA[ 3 ] << miA[ 4 ];
	}

	void funcion( int miArray[] )  {
	    miArray[ 0 ] = 5;  // Las modificaciones quedarán.

	    miArray[ 3 ] = 5; 
	} 



QTextEdit
=========

- Un QWidget que muestra texto plano o enriquecido
- Puede mostrar imágenes, listas y tablas
- La barra de desplazamiento es automática
- Interpreta tags HTML
- Seteamos texto con setPlainText()



QGroupBox
^^^^^^^^^ 

.. figure:: imagenes/qgroupbox.png

.. code-block::

	QGroupBox * grupo = new QGroupBox( "Texto" );
	QGridLayout * layout = new QGridLayout;
	
	layout->addWidget( label, 0, 0 );
	layout->addWidget( usuario, 1, 0, 1, 2 );
	layout->addWidget( clave, 2, 0, 1, 2 );
	
	grupo->setLayout( layout );




El preprocesador
^^^^^^^^^^^^^^^^

-	Analiza el archivo fuente antes de la compilación real
-	Realiza las sustituciones de macros
-	Una macro es un patrón de sustitución formado por expresiones textuales
-	Procesa las directivas (``#include``, ``#define``, ``#ifndef``, ...)
-	Elimina los comentarios.


**Directivas #ifdef #endif #ifndef**

- Con ``#ifdef`` si la macro está definida, entonces hace lo siguiente hasta encontrar un ``#endif``
- ``#ifndef`` pregunta si no está definida


**Directiva #include**

- Inserta archivos
- Influye sobre el ámbito y los identificadores

.. code-block::

	#include <nombre de fichero cabecera>
	#include "nombre de fichero de cabecera"

**Directiva #define**

- Define macros para sustituir cada vez que se encuentre el identificador.

.. code-block::

	#define identificador <secuencia>
	
-	Si 'secuencia' no existe, el identificador será eliminado cada vez que aparezca
-	No es necesario añadir un punto y coma al final
-	Termina en el primer retorno de línea encontrado



Guardián de inclusión múltiple
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Este problema se soluciona con el uso del **Guardián de inclusión múltiple**:

.. code-block::

	#ifndef PRINCIPAL_H
	#define PRINCIPAL_H

	// . . . 

	#endif // PRINCIPAL_H





Ejercicio 05 - Login sin QtDesigner
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Replicar el ejemplo del login en un empty project
- Grabar un video explicando el desarrollo de esta aplicación y subirlo a Youtube como No listado
- El video referencia es: `Login en empty project 2025 <https://youtu.be/Gdo6NcdOuPo>`_


Ejercicio 06 - Login con QtDesigner
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Replicar el ejemplo del login en QtDesigner
- Grabar un video explicando el desarrollo de esta aplicación y subirlo a Youtube como No listado
- Video referencia de 2026: `Login con QtDesigner 2026 <https://youtu.be/rcNz_rKD7PQ>`_
- Video referencia de 2025: `Login con QtDesigner 2025 <https://youtu.be/9Z208vj-jCw>`_




