Clase 02 - 11 de marzo de 2026
=============================


Registro en video de algunos temas de la clase de hoy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`std C y std C++ 2021 <https://www.youtube.com/watch?v=GrOLHLHcZqg>`_

`Espacio de nombres 2021 <https://www.youtube.com/watch?v=oUVACqK4ssg>`_ 

`std namespace vector list 2022 <https://www.youtube.com/watch?v=7ORVHLxFvRM>`_ 


Biblioteca estándar de C++
==========================

La biblioteca estándar de C++ se encuentra en el **espacio de nombres ``std``**.

Ejemplos:

.. code-block:: cpp

    #include <iostream>

    std::cout << "Hola mundo" << std::endl;


Algunos ejemplos de cabeceras de la biblioteca estándar:

.. code-block:: cpp

    #include <vector>
    #include <string>
    #include <iostream>




Espacio de nombres (namespace)
==============================

- Permite agrupar declaraciones (de clases, funciones, etc.).
- Permite declarar identificadores (nombre de variables) sin que se solapen. Es decir, identificadores iguales en distinto namespace.
- Se pueden incluir las definiciones en un namespace pero mejor no.
- Un espacio de nombre es un ámbito.

Ejemplos con namespace
======================

**Ejemplo 1**

.. code-block::

	#include <iostream>
	using namespace std;

	namespace enteros  { int valor = 5; }
	namespace decimales { float valor = 5.14f; }

	int main()  {
	    cout << enteros::valor << endl;
	    cout << decimales::valor << endl;
	    return 0;
	}

**Ejemplo 2**

.. code-block::

	#include <iostream>
	using namespace std;

	namespace a  { int x = 1; }
	namespace b  { int x = 2; }

	int main()  {
	    using a::x;
	    cout << x << endl;    // a::x
	    cout << b::x << endl; // b::x
	    return 0;
	}




Ejercicio del dia (equipo)
==========================

1) Buscar proveedores de VPS y costos
	- Investigar al menos 3 opciones.
	- Registrar plan, RAM, vCPU, almacenamiento, region y costo mensual.

2) Dominio en NIC.AR
	- Revisar costos de registro/renovacion.
	- Proponer 2 nombres de dominio relacionados al proyecto.

3) Definir integrantes del equipo
	- Confirmar nombres y roles iniciales.

4) Definir idea del proyecto
	- Elegir una de las opciones propuestas por el docente o proponer una nueva.
	- Describir la idea en 3 lineas.

Opciones de proyectos como referencia
=====================================

- TP1: Analizador Inteligente de Imagenes. App que analiza imagenes con IA y muestra descripcion/etiquetas.
- TP2: Analizador de CVs para seleccion de personal. App que resume CVs y sugiere ranking.
- TP3: Analizador de reuniones grabadas. App que resume transcripciones y lista tareas.
- TP4: Planificador de tareas tecnicas. App que convierte requerimientos en plan de tareas.
- TP5: Transcriptor inteligente de dialogos desde audio. App que separa dialogos por hablante.
- TP6: Generador de imagenes a partir de descripcion. App que crea imagenes desde texto.
- TP7: Asistente de resolucion de problemas de programacion. App que explica y sugiere mejoras de codigo.

5) Elegir dominio del equipo
	- Definir un nombre final y justificarlo en una linea.

6) Instalar Qt Creator
	- Instalar Qt, Qt Creator y MinGW 64-bit.
	- Abrir un proyecto vacio para verificar que compila.

7) Configurar Copilot en Qt Creator
	- Dejar Copilot funcionando y probado.

8) Acceso a GPT-5.2 Codex
	- Verificar si necesitan plan pago para usar GPT-5.2 Codex.
	- Si es necesario, definir quien lo contrata y el costo.
	- Probar GPT-5.2 Codex en VS Code.

Entregables
===========

- Tabla breve con opciones de VPS y costos.
- Integrantes del equipo.
- Idea del proyecto (3 lineas).
- Captura o evidencia de Qt Creator funcionando.
- Nombre de dominio elegido y costos de NIC.AR.
- Estado de Copilot y acceso a GPT-5.2 Codex.
- Evidencia de GPT-5.2 Codex en VS Code.

Lo que no se logre hoy debe completarse y traerlo para la proxima clase.


