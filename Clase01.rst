.. -*- coding: utf-8 -*-

Clase 01 - 9 de marzo de 2026
=============================

Temas de la clase
=================

- Concepto general de la materia
- Equipos de trabajo
- Herramientas de trabajo (GitHub, VS Code y Copilot, Qt, servidor en la nube, dominio propio)
- Proyecto integrador
- Enfoque de aprendizaje
- Contenidos centrales y evaluaciones


Registro en video de algunos temas de la clase de hoy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`Library, Librería, Biblioteca 2021 <https://www.youtube.com/watch?v=k9ZZSSWuX6E>`_


Concepto general de la materia
==============================

Esta materia se desarrollará con una modalidad de trabajo similar a un **entorno laboral real de desarrollo de software**.

La clase funcionará como una empresa de desarrollo.

- El docente cumple el rol de **director técnico del proyecto**.
- Los estudiantes trabajan en **equipos de desarrollo**.
- Cada equipo tendrá **un proyecto propio durante el cuatrimestre**.

Durante el curso trabajaremos utilizando herramientas y metodologías que se utilizan actualmente en la industria del software.

El objetivo es que los estudiantes aprendan no solo a programar, sino también a:

- diseñar software
- trabajar en equipo
- utilizar herramientas profesionales
- comprender la Programación Orientada a Objetos


Equipos de trabajo
==================

Los estudiantes deberán organizarse en **equipos de trabajo**.

Condiciones:

- Los equipos serán de **3 estudiantes**.
- Solo en caso de que la cantidad total de alumnos no permita formar únicamente equipos de tres, se permitirá uno o dos equipos de dos estudiantes.
- Cada equipo tendrá **un proyecto propio**.

Los equipos deben quedar definidos durante las **primeras clases**.


Herramientas de trabajo
=======================

Durante el cuatrimestre se utilizarán herramientas profesionales de desarrollo.

GitHub
======

Cada equipo deberá:

- Crear un **repositorio en GitHub**
- Trabajar con **ramas**
- Realizar **commits**
- Integrar cambios mediante **pull requests**
- Mantener una **rama principal estable**

El docente deberá ser agregado como **colaborador del repositorio**.

La rama principal representará siempre el **sistema funcionando**.


Visual Studio Code y Copilot
============================

Cada estudiante deberá contar con acceso a **GitHub Copilot**.

Copilot se utilizará como **herramienta de asistencia para programación**.

El objetivo del curso es aprender a:

- diseñar software correctamente
- analizar código generado por IA
- corregirlo
- mejorarlo
- integrarlo en sistemas reales


Herramientas de desarrollo C++ y Qt (Desktop)
=============================================

Se utilizarán herramientas específicas para desarrollo de aplicaciones desktop:

- Biblioteca estándar de C++
- Compilador **MinGW**
- Biblioteca **Qt**
- **Qt Creator**
- Copilot integrado en Qt Creator


Servidor en la nube
===================

Cada equipo deberá contratar un **servidor en la nube** para ejecutar su proyecto.

Puede utilizarse cualquier proveedor, por ejemplo:

- AWS
- Google Cloud
- otros proveedores equivalentes

Requisitos mínimos recomendados:

- **2 a 4 GB de RAM**
- **2 vCPU**

Este servidor deberá permanecer activo durante el cuatrimestre.


Dominio propio
==============

Cada equipo deberá registrar un **dominio propio en NIC.AR**.

Este dominio deberá apuntar al sistema desplegado en la nube.


Proyecto integrador
===================

Cada equipo desarrollará un sistema completo compuesto por varias partes.

Frontend
========

- React
- TypeScript
- Ant Design

Backend
=======

- API REST desarrollada con **FastAPI**

Infraestructura
==============

- Servidor en la nube
- Dominio propio
- Sistema accesible públicamente

Cliente Desktop
===============

Cada proyecto deberá incluir además una **aplicación desktop desarrollada en C++ utilizando Qt**.

Este cliente será parte central de la evaluación de la materia.


Enfoque de aprendizaje
======================

La modalidad del curso será:

**Primero práctica, luego teoría.**

El proceso será:

1) Construir algo que funcione  
2) Detectar problemas o limitaciones  
3) Introducir los conceptos teóricos que permiten resolverlos  

De esta forma se van comprendiendo los conceptos de Programación Orientada a Objetos.


Contenidos centrales de la materia
==================================

El foco académico del curso es:

**Programación Orientada a Objetos en C++ utilizando Qt.**

Los principales temas que se desarrollarán son:

- creación de clases
- encapsulamiento
- herencia
- herencia múltiple
- polimorfismo
- funciones virtuales
- funciones virtuales puras
- clases abstractas
- espacios de nombres
- uso de contenedores como ``vector`` y ``list``
- diseño de bibliotecas propias
- desarrollo de interfaces gráficas con Qt


Evaluaciones
============

La materia tendrá dos instancias evaluativas principales.

Regularidad, promoción y coloquio
=================================

- La materia se promociona bajo la modalidad de la UBP.
- El coloquio se debe rendir dentro del cursado de la materia, no en una fecha de examen final.
- El coloquio sigue la metodología de un final: parte teórica y parte oral.
- Los temas del coloquio se acuerdan con anticipación.

Comunicaciones
==============

:Meet y WhatsApp para comunicaciones:
    - `https://meet.google.com/vyf-bsai-uvq <https://meet.google.com/vyf-bsai-uvq>`_
    - `WhatsApp 2026 <https://chat.whatsapp.com/IKlnsY97gig3fC2rDvQmxY>`_

.. image:: imagenes/whatsapp_2026_qr.png
   :alt: QR del grupo de WhatsApp 2026
   :width: 250px




Primer parcial (individual)
===========================

Cada estudiante deberá desarrollar una **aplicación desktop en C++ utilizando Qt**.

Se entregará un **enunciado del problema** y el estudiante deberá resolverlo.

Podrán utilizar herramientas como:

- Copilot
- ChatGPT
- Gemini
- otras herramientas de asistencia

Se evaluará:

- diseño de clases
- uso correcto de Programación Orientada a Objetos
- estructura del programa
- funcionamiento del sistema


Segundo parcial (proyecto integrador)
========================================

Cada equipo presentará su **proyecto completo**.

El proyecto deberá incluir:

- frontend
- API backend
- servidor en la nube
- dominio propio
- cliente desktop en C++ con Qt
- repositorio GitHub correctamente organizado

Se evaluará:

- arquitectura del sistema
- calidad del código
- uso de herramientas profesionales
- trabajo en equipo


Examen final
============

El examen final tendrá dos partes.

Parte práctica
==============

Resolución de **desafíos de programación en C++**.


Parte oral
==========

Explicación de conceptos teóricos como:

- herencia
- polimorfismo
- funciones virtuales
- clases abstractas
- diseño de clases


Instalación de herramientas
===========================

Qt
==

Instalar:

- Biblioteca de **Qt**
- **Qt Creator**
- compilador **MinGW 64-bit**


OpenSSL
=======

Descargar instalador desde:

https://slproweb.com/products/Win32OpenSSL.html

Seleccionar:

Win64 OpenSSL v3.x



Próximos pasos
==============

Para la próxima clase cada equipo deberá:

1) Formar el **grupo de trabajo**  
2) Crear el **repositorio en GitHub**  
3) Agregar al docente como colaborador  
4) Definir la **idea del proyecto del grupo** con las opciones que menciona el docente  
5) Instalar **Qt Creator**, la **biblioteca Qt** y **MinGW 64-bit**

Durante las próximas clases comenzaremos a desarrollar aplicaciones en **C++ y Qt**, incorporando progresivamente los conceptos de **Programación Orientada a Objetos**.
