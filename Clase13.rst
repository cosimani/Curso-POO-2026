Clase 13 - 27 de abril de 2026
==============================



Registro en video de algunos temas de la clase de hoy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`Polimorfismo función virtual 2021 <https://youtu.be/wT_LfW-Ao0A>`_

`Polimorfismo - QtDesigner y métodos virtuales de QWidget 2023 <https://youtu.be/idc1aCpYUgg>`_

`Funciones virtuales 2023 <https://youtu.be/a5-p12-jscc>`_


Polimorfismo
============

- Lo utilizamos con punteros.
- Nos permite acceder a objetos de la clase derivada usando un puntero a la clase base.
- Sin embargo, sólo podemos acceder a datos y funciones que existan en la clase base.
- Los datos y funciones propias de la derivada quedan inaccesibles.

.. code-block::

	class Persona  {
	public:
	    Persona( QString nombre ) : nombre( nombre )  {  }
	    QString verNombre()  {  return "Nombre: " + nombre;  }

	protected:  // Para acceso desde las clases derivadas
	    QString nombre;
	};

	class Empleado : public Persona  {
	public:
	    Empleado( QString nombre ) : Persona( nombre )  {  }
	    QString verNombre()  {  return "Empleado: " + nombre;  }
	    void mostrarAlgo()  {  qDebug() << "Algo";  }
	};

	class Estudiante : public Persona  {
	public:
	    Estudiante( QString nombre ) : Persona( nombre )  {  }
	    QString verNombre()  {  return "Estudiante: " + nombre;  }
	};


	#include <QApplication>
	#include "persona.h"
	#include <QDebug>

	int main( int argc, char** argv )  {
	    QApplication a(argc, argv);

	    {
	    Persona * jose = new Estudiante( "Jose" );
	    Persona * carlos = new Empleado( "Carlos" );

	    qDebug() << carlos->verNombre();
	    qDebug() << jose->verNombre();
	    carlos->mostrarAlgo();  // Muestra algo? 

	    delete jose;
	    delete carlos;
	    }

	    return a.exec();
	}
	


Funciones virtuales
===================

- Puede ser interesante llamar a la función de la derivada (en polimorfismo).
- Al declarar una función como virtual en la clase base, si se superpone en la derivada, al invocar usando el puntero a la clase base, se ejecuta la versión de la derivada.

.. code-block::

	class Persona  {
	public:
	    Persona( QString nombre ) : nombre( nombre )  {  }
	    virtual QString verNombre()  {  return "Persona: " + nombre;  }  // Y si no fuera virtual?

	protected:  
	    QString nombre;
	};

	class Empleado : public Persona  {
	public:
	    Empleado( QString nombre ) : Persona( nombre )  {  }
	    QString verNombre()  {  return "Empleado: " + nombre;  }
	};


	#include <QApplication>
	#include "personal.h"
	#include <QDebug>

	int main( int argc, char** argv )  {
	    QApplication a( argc, argv) ;

	    {
	    Persona *carlos = new Empleado( "Carlos" );

	    qDebug() << carlos->verNombre();  // Qué publica?

	    delete carlos;
	    }

	    return a.exec();
	}






Métodos virtuales de QWidget para capturar eventos
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Estos métodos pueden ser reimplementados en una clase derivada para recibir los eventos.

.. code-block::

	virtual void mouseDoubleClickEvent( QMouseEvent * event );
	virtual void mouseMoveEvent( QMouseEvent * event );
	virtual void mousePressEvent( QMouseEvent * event );
	virtual void mouseReleaseEvent( QMouseEvent * event );
	virtual void keyPressEvent( QKeyEvent * event );
	virtual void keyReleaseEvent( QKeyEvent * event );
	virtual void resizeEvent( QResizeEvent * event );
	virtual void moveEvent( QMoveEvent * event );
	virtual void closeEvent( QCloseEvent * event );
	virtual void hideEvent( QHideEvent * event );
	virtual void showEvent( QShowEvent * event );
	virtual void paintEvent( QPaintEvent * event );




Ejercicio 08 - Editor multilenguaje
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Login inicial con usuario ``admin:1234`` y bloqueo temporal tras 3 intentos fallidos.
- Clase base abstracta ``Pantalla`` con interfaz común y clases derivadas concretas: ``Login``, ``EditorPrincipal`` y ``ModoBloqueado``.
- Uso obligatorio de polimorfismo: el flujo de la aplicación debe trabajar contra punteros o referencias de la clase base.
- Definición de funciones virtuales puras en la clase base (por ejemplo: ``inicializarUI()``, ``conectarEventos()``, ``cargarDatos()``, ``validarEstado()`` y ``registrarEvento()``) y sobrescritura obligatoria en cada derivada.
- Editor principal con selector de lenguaje: C++, Python y Java.
- Jerarquía polimórfica para validación de sintaxis:

	- ``ValidadorSintaxis`` (abstracta)
	- ``ValidadorCpp``, ``ValidadorPython`` y ``ValidadorJava`` (derivadas)

- Validación de sintaxis por línea: la verificación debe ejecutarse al abandonar la línea que se está editando.
- Resaltado de error en rojo cuando la línea sea inválida, con mensaje de diagnóstico amigable en la UI.
- Captura y redefinición de eventos en las clases derivadas:

	- ``keyPressEvent`` para atajos del editor.
	- ``mousePressEvent`` para interacción de cursor y selección.
	- ``resizeEvent`` para adaptación visual del contenido.
	- ``closeEvent`` para confirmación de salida y guardado.
	- ``focusInEvent`` y ``focusOutEvent`` para control de edición y disparo de validación.

- Redefinición consciente de eventos: cada pantalla debe implementar un comportamiento distinto según su responsabilidad.
- Registro de eventos en archivo de log con fecha y descripción de cada acción relevante.
- Lectura de configuración desde archivo (usuario inicial, tiempo de bloqueo, lenguaje por defecto y ruta de exportación).
- Soporte offline: la aplicación debe funcionar sin internet y sin dependencias de servicios remotos.
- Uso obligatorio de ``signals/slots`` tal como lo vimos en clase.
- Luego de un usuario válido, se abre la ventana principal en full screen.
- Exportación final a un único archivo JPG que contenga todo el código escrito, en forma legible y respetando saltos de línea.
- Para que no quede vacía la ventana principal, agregar un panel lateral con currículum estilo LinkedIn: foto, descripción breve, habilidades y contacto.

