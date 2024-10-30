# Actividad_participacion_10
 Ejercicio validador de clave

Ejercicio Validador de Clave
Para este ejercicio vas a suponer que trabajas en un proyecto donde te asignan la tarea de desarrollar un módulo para la validación de una clave.

En el diseño del módulo para validación de clave se establecieron dos reglas de validación, las cuales fueron nombradas como Validación Ganímedes y Validación Calisto.

1. Validación Ganímedes
Esta regla de validación verifica si una clave cumple con lo siguiente:

Tiene una longitud de más de 8 caracteres
Tiene al menos una letra mayúscula
Tiene al menos una letra minúscula
Tiene al menos un número
Tiene al menos un caracter especial que puede ser cualquiera de @, _, #, $ o %
2. Validación Calisto
Esta regla de validación verifica si una clave cumple con lo siguiente:

Tiene una longitud de más de 6 caracteres
Tiene al menos un número
Tiene la palabra calisto escrita con al menos dos letras en mayúscula, pero no todas. Por ejemplo, cAliStO sería válida.
Cada condición de las reglas se verifica una por una y en el orden en el que aparecen en la descripción. Esto quiere decir que si una condición no se cumple, no se verifican las siguientes.

Con base en los requisitos del problema, el arquitecto de software del proyecto realizó el siguiente diseño para el módulo de validación de claves:

Modelo de clases

Tu misión es implementar el modelo planteado por el arquitecto de software. Para lograr tu misión debes tener en cuenta lo siguiente:

La clase ReglaValidacion es una clase abstracta y su método es_valida es igualmente abstracto.
El método _validar_longitud de la clase ReglaValidacion implementa la lógica para verificar la longitud de la clave. Para implementar dicho método debes tener en cuenta el atributo _longitud_esperada, el cual es inicializado en el constructor de la clase e indica la longitud que la clave debe superar.
Los métodos _contiene_mayuscula, _contiene_minuscula y _contiene_numero de la clase ReglaValidacion implementan correspondientemente la lógica que verifica si una clave tiene una letra mayúscula, tiene una letra minúscula y tiene un número. Para implementar dichos métodos puedes utilizar los métodos de la clase str isupper(), islower() e isdigit().
La clase ReglaValidacionGanimedes tiene un método contiene_caracter_especial donde debes implementar la lógica para verificar si una clave contiene al menos uno de los caracteres especiales @ _ # $ %.
La clase ReglaValidacionCalisto tiene un método contiene_calisto donde debes implementar la lógica para verificar si una clave contiene la palabra calisto escrita con al menos dos letras mayúsculas, pero no con todas las letras mayúsculas. Para implementar dicho método puedes utilizar el método find() de la clase str
Los métodos es_valida en las clases ReglaValidacionGanimedes y ReglaValidacionCalisto son las implementaciones del método abstracto de la clase padre. En estos métodos debes implementar las reglas correspondientes a cada tipo de validación, utilizando los demás métodos donde están definidas cada una de las reglas.
Los métodos es_valida en las clases ReglaValidacionGanimedes y ReglaValidacionCalisto deben arrojar excepciones para los casos en que no se cumplan las reglas. En el proyecto hay una jerarquía de tipos de excepciones (en el módulo errores.py), correspondientes a cada regla, que debes utilizar para generar las excepciones. Las reglas se deben verificar en el orden en el que se especifican en la descripción. En el caso en el que se cumplan todas las reglas, el método debe retornar True.
El método es_valida de la clase Validador debe retornar el resultado de invocar el método es_valida en el objeto regla que tiene como atributo.
Para realizar la actividad puedes hacer fork del siguiente repositorio: https://github.com/jahlonteaching/EjercicioValidadorClave.git

En el proyecto que se encuentra en el repositorio, debes implementar el código de la funcionalidad solicitada en el archivo validador.py que se encuentra en el paquete validadorclave.modelo.

Ten en cuenta
El proyecto incluye un conjunto de pruebas que puedes utilizar para verificar el cumplimiento de los requisitos establecidos. Para ejecutar las pruebas, debes instalar la dependencia pytest (pip install pytest).
Para que las pruebas funcionen adecuadamente debes implementar el código respetando los nombres y la definición de las clases y los métodos que se presentan en el diagrama.
El desarrollo del ejercicio solo se puede hacer en PyCharm o en Visual Studio Code. Pueden utilizar todas las ayudas que el IDE les presta, pero no pueden hacer consultas en internet, excepto la documentación de los métodos de la clase str en el siguiente enlace: https://docs.python.org/es/3/library/stdtypes.html#string-methods. 