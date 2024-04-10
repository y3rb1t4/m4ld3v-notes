# Introducción al desarrollo de malware


### ¿Qué es el malware?

El malware es un tipo de software diseñado específicamente para realizar acciones maliciosas, como obtener acceso no autorizado a una máquina o robar datos confidenciales de una máquina. El término "malware" a menudo se asocia con conductas ilegales o delictivas, pero también puede ser utilizado por piratas informáticos éticos, como probadores de penetración y miembros del equipo rojo, para una evaluación de seguridad autorizada de una organización.



### ¿Por qué aprender a desarrollar malware?
Hay varias razones por las que alguien querría aprender a desarrollar malware. Desde una perspectiva de seguridad ofensiva, los evaluadores a menudo necesitarán realizar ciertas tareas maliciosas en el entorno de un cliente. Los evaluadores generalmente tienen tres opciones principales cuando se trata de los tipos de herramientas utilizadas en un compromiso:

1. Herramientas de código abierto (OST): estas herramientas generalmente están firmadas por proveedores de seguridad y se detectan en cualquier organización madura o con una protección decente. No siempre son confiables cuando realizan una evaluación de seguridad ofensiva.

2. Compra de herramientas: los equipos con presupuestos más grandes a menudo optarán por comprar herramientas para ahorrar tiempo valioso durante las interacciones. Al igual que las herramientas personalizadas, estas generalmente son de código cerrado y tienen más posibilidades de evadir las soluciones de seguridad.

3. Desarrollo de herramientas personalizadas: debido a que estas herramientas están diseñadas a medida, no han sido analizadas ni firmadas por proveedores de seguridad, lo que le da al equipo atacante una ventaja en lo que respecta a la detección. Aquí es donde el conocimiento del desarrollo de malware se vuelve fundamental para una evaluación de seguridad ofensiva más exitosa.

### ¿Qué lenguaje de programación se debe utilizar?
Técnicamente hablando, se puede utilizar cualquier lenguaje de programación para crear malware como Python, PowerShell, C#, C, C++ y Go. Dicho esto, existen algunas razones por las que algunos lenguajes de programación prevalecen sobre otros cuando se trata de desarrollo de malware y, por lo general, se reduce a los siguientes puntos:

- Ciertos lenguajes de programación son más difíciles de aplicar mediante ingeniería inversa. Siempre debe ser parte del objetivo del atacante garantizar que los defensores tengan una comprensión limitada de cómo se comporta el malware.

- Algunos lenguajes de programación requieren requisitos previos en el sistema de destino. Por ejemplo, ejecutar un script de Python requiere un intérprete presente en la máquina de destino. Sin el intérprete de Python presente en la máquina, es imposible ejecutar malware basado en Python.

- Dependiendo del lenguaje de programación, el tamaño del archivo generado será diferente.

### Lenguajes de programación de alto nivel versus bajo nivel
Los lenguajes de programación se pueden clasificar en dos grupos diferentes, de alto nivel y de bajo nivel.

- Alto nivel: generalmente más abstraído del sistema operativo, menos eficiente con la memoria y proporciona al desarrollador menos control general debido a la abstracción de varias funciones complejas. Un ejemplo de lenguaje de programación de alto nivel es Python.

- Bajo Nivel: proporciona una forma de interactuar con el sistema operativo a un nivel íntimo y proporciona al desarrollador más libertad al interactuar con el sistema. Un ejemplo de lenguaje de programación de bajo nivel es C.

Dadas las explicaciones anteriores, debería quedar claro por qué los lenguajes de programación de bajo nivel han sido la opción preferida en el desarrollo de malware, especialmente cuando se dirige a máquinas con Windows.

### Desarrollo de malware para Windows.

La escena del desarrollo de malware para Windows ha cambiado en los últimos años y ahora está muy centrada en evadir soluciones de seguridad basadas en host como Antivirus (AV) y Endpoint Detección y Respuesta (EDR). Con el avance de la tecnología, ya no es suficiente crear malware que ejecute comandos sospechosos o realice acciones "similares a malware".


### Ciclo de vida del desarrollo de malware.

Básicamente, el malware es un software diseñado para realizar determinadas acciones. Las implementaciones de software exitosas requieren un proceso conocido como ciclo de vida de desarrollo de software (SDLC). De manera similar, un malware complejo y bien construido requerirá una versión personalizada del SDLC denominada Ciclo de vida de desarrollo de malware (MDLC).


Desarrollo: comience el desarrollo o perfeccionamiento de la funcionalidad dentro del malware.

Pruebas: realice pruebas para descubrir errores ocultos dentro del código desarrollado hasta ahora.

Pruebas AV/EDR sin conexión: ejecute el malware desarrollado contra tantos productos de seguridad como sea posible. Es importante que las pruebas se realicen fuera de línea para garantizar que no se envíen muestras a los proveedores de seguridad. Con Microsoft Defender, esto se logra deshabilitando los envíos automatizados de muestras y la opción de protección entregada en la nube.

Pruebas AV/EDR en línea: ejecute el malware desarrollado contra los productos de seguridad con conectividad a Internet. Los motores en la nube suelen ser componentes clave en los AV/EDR y, por lo tanto, probar su malware contra estos componentes es crucial para obtener resultados más precisos. Tenga cuidado, ya que este paso puede provocar que se envíen muestras al motor en la nube de la solución de seguridad.

Análisis de IoC (indicadores de compromiso): en esta etapa, usted se convierte en el cazador de amenazas o analista de malware. Analice el malware y extraiga los IoC que potencialmente puedan usarse para detectar o firmar el malware.

