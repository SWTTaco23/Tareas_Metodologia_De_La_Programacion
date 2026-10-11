# Investigación sobre configuraciones de robots móviles

**Nombre:** Fernando Emir Walle Hernandez  

**Matrícula:** 2630316  

**Asignatura:** Metodología de la programación  

**Fecha:** 11 de octubre del 2026

## 1. Conceptos básicos

### ¿Qué es un robot móvil?

Un robot móvil es una máquina programable que puede desplazarse de un lugar a otro. Puede utilizar ruedas, patas, orugas u otros mecanismos, además de sensores y un controlador para realizar sus tareas.

### Diferencia entre un robot móvil y un manipulador fijo

Un robot móvil cambia de ubicación al desplazar su base. Un manipulador fijo permanece instalado en un lugar y mueve sus articulaciones para trabajar dentro de una zona determinada.

Por ejemplo, un robot móvil puede transportar materiales entre estaciones, mientras que un brazo fijo puede ensamblar piezas que llegan a su mesa de trabajo.

También existen manipuladores móviles, que combinan una base que se desplaza con un brazo robótico.

### Función del sistema de locomoción

El sistema de locomoción permite que el robot se desplace y cambie su orientación. Incluye los elementos mecánicos y actuadores que producen el movimiento, como ruedas, motores, ejes y transmisiones.

### ¿Qué significa movilidad omnidireccional?

Significa que el robot puede trasladarse en cualquier dirección del plano sin tener que girar primero para apuntar hacia ella. Por ejemplo, puede desplazarse hacia un costado manteniendo el frente en la misma dirección.

Una plataforma omnidireccional correctamente configurada también puede combinar traslación y giro.

### Relación entre las ruedas y los movimientos

La posición, orientación y tipo de ruedas determinan qué movimientos puede realizar el robot. Las ruedas convencionales se oponen al deslizamiento lateral, mientras que las ruedas Omni y Mecanum incorporan rodillos que permiten movimiento en otra dirección.

No basta con colocar ruedas especiales: es necesario distribuirlas correctamente y coordinar sus velocidades.

### Aplicaciones de los robots móviles

- Transporte de materiales dentro de almacenes.
- Inspección de instalaciones.
- Limpieza de pisos.
- Investigación y enseñanza de robótica.
- Exploración de lugares peligrosos.

## 2. Robot diferencial con rueda de castor

### Distribución de las ruedas

Esta configuración tiene dos ruedas motrices, una a cada lado del robot. Sus ejes están alineados y cada rueda cuenta con un motor que puede controlarse de manera independiente.

Una rueda de castor, también llamada rueda loca, proporciona un tercer punto de apoyo. Normalmente no tiene motor y gira libremente para acomodarse al movimiento.

También puede utilizarse un apoyo esférico o ball caster, cuyo funcionamiento mecánico es distinto al de una rueda orientable, pero cumple una función de soporte similar.

### ¿Cómo se mueve?

- **Avance recto:** ambas ruedas tienen la misma velocidad hacia adelante.
- **Retroceso recto:** ambas tienen la misma velocidad hacia atrás.
- **Curva hacia la izquierda al avanzar:** la rueda derecha se mueve más rápido.
- **Curva hacia la derecha al avanzar:** la rueda izquierda se mueve más rápido.
- **Giro sobre su eje:** las ruedas se mueven en sentidos opuestos con velocidades de igual magnitud.

Cuando una rueda avanza más rápido que la otra, el robot describe una curva. Si una permanece detenida, el robot gira aproximadamente alrededor del punto de contacto de esa rueda.

El ancho entre las ruedas influye en la relación entre sus velocidades y la velocidad de giro del robot [1].

### Esquema visto desde arriba

**Frente y sentido de avance: ↑**

| Lado izquierdo | Centro del robot | Lado derecho |
| :---: | :---: | :---: |
| | Frente ↑ | |
| Rueda izquierda ↕ | ⊙ Eje vertical de giro | Rueda derecha ↕ |
| | Rueda de castor ○ | |

**Leyenda:**

- ↕: dirección de rodamiento de las ruedas motrices.
- ○: rueda de apoyo sin motor.
- ⊙: eje vertical aproximado para el giro en el lugar.
- El eje de giro está en el punto medio entre las ruedas motrices, no necesariamente en el centro geométrico del chasis.

### Tabla de movimientos

En esta tabla, “avanza” significa que la rueda gira en el sentido que impulsaría su lado hacia el frente. Para los giros en el lugar se consideran velocidades iguales en magnitud.

| Rueda izquierda | Rueda derecha | Movimiento del robot |
| --- | --- | --- |
| Avanza | Avanza | Avanza en línea recta si las velocidades son iguales. |
| Detenida | Avanza | Gira hacia la izquierda alrededor de la rueda izquierda. |
| Avanza | Detenida | Gira hacia la derecha alrededor de la rueda derecha. |
| Avanza | Retrocede | Gira sobre su eje hacia la derecha. |
| Retrocede | Avanza | Gira sobre su eje hacia la izquierda. |
| Retrocede | Retrocede | Retrocede en línea recta si las velocidades son iguales. |

### Ventajas

- Solo necesita dos motores para la locomoción.
- Tiene una estructura sencilla.
- Permite girar sin avanzar.
- Es adecuado para aprender programación y control.

### Limitaciones

- No puede desplazarse directamente hacia un costado.
- La rueda de castor puede dificultar el movimiento sobre obstáculos.
- Las diferencias reales entre motores pueden desviar el avance.
- El deslizamiento afecta la estimación de posición.

### Aplicaciones

Se utiliza en robots educativos, plataformas de investigación y algunos robots de limpieza o transporte.

## 3. Robots omnidireccionales con ruedas Omni

### Construcción de una rueda Omni

Una rueda Omni tiene una rueda principal accionada por un motor y pequeños rodillos distribuidos alrededor de su perímetro.

Los rodillos giran libremente y permiten que la rueda se desplace en una dirección perpendicular a su dirección de rodamiento motorizado [2].

### Función de los rodillos

La rueda genera fuerza principalmente en su dirección de rodamiento. En la dirección transversal, los rodillos pueden girar sin que el motor tenga que hacerlo.

Esto reduce la resistencia al desplazamiento lateral. No significa que la fricción desaparezca por completo.

Una rueda convencional tendría que deslizar sobre el suelo para moverse transversalmente. En una rueda Omni, los rodillos permiten ese movimiento mediante rodadura.

### Configuración de tres ruedas

#### Distribución

Una distribución habitual utiliza tres ruedas alrededor del centro, separadas aproximadamente 120°. Sus ejes apuntan radialmente y sus direcciones de rodamiento son tangentes a una circunferencia imaginaria.

Cada rueda necesita un motor independiente. Esta disposición permite controlar avance, desplazamiento lateral y giro [3], [4].

#### Esquema visto desde arriba

**Frente: ↑**

| Zona izquierda | Centro | Zona derecha |
| :---: | :---: | :---: |
| | Rueda 1 ↔ | |
| | Centro ⊙ | |
| Rueda 2 ↗↙ | | Rueda 3 ↖↘ |

Las tres posiciones están separadas aproximadamente 120° alrededor del centro. Las flechas representan las direcciones de rodamiento motorizado, no los ejes de las ruedas.

#### Movimientos

- **Hacia adelante:** en el esquema mostrado, las ruedas 2 y 3 aportan componentes hacia el frente; sus componentes laterales se compensan.
- **Hacia atrás:** se invierten las velocidades del avance.
- **Lateralmente:** se combinan las tres velocidades para generar una traslación horizontal sin giro.
- **En diagonal:** se combinan las componentes de avance y desplazamiento lateral.
- **Sobre su eje:** las tres ruedas impulsan tangencialmente en el mismo sentido alrededor del centro.

Para girar, “mismo sentido” significa el mismo sentido tangencial alrededor del robot. No implica necesariamente enviar la misma polaridad eléctrica a todos los motores.

Si las tres ruedas tienen velocidades diferentes, puede obtenerse una traslación, una rotación o una combinación. El resultado depende del sentido y valor de cada velocidad.

### Configuración de cuatro ruedas

#### Distribución

Una opción consiste en colocar una rueda en cada lado del chasis, con sus direcciones de rodamiento tangentes alrededor del centro. Las posiciones están separadas aproximadamente 90° [4].

Esta configuración es distinta de colocar cuatro ruedas Omni paralelas como las de un automóvil.

#### Esquema visto desde arriba

**Frente: ↑**

| Izquierda | Centro | Derecha |
| :---: | :---: | :---: |
| | Rueda delantera ↔ | |
| Rueda izquierda ↕ | Centro ⊙ | Rueda derecha ↕ |
| | Rueda trasera ↔ | |

#### Combinación de velocidades

En este arreglo:

- Las ruedas izquierda y derecha generan principalmente avance y retroceso.
- Las ruedas delantera y trasera generan principalmente desplazamiento lateral.
- Para girar, las cuatro producen movimiento tangencial alrededor del centro.
- Para avanzar en diagonal se combinan las dos componentes de traslación.

Las velocidades deben ser compatibles entre sí. Órdenes contradictorias pueden provocar deslizamiento y esfuerzos entre ruedas.

#### Diferencias respecto a tres ruedas

Tres ruedas permiten controlar los tres movimientos del plano con tres motores. Cuatro ruedas añaden un punto de apoyo y un motor, pero requieren coordinar una velocidad adicional.

#### Ventajas

- Permite desplazamiento lateral y giro.
- Puede ofrecer una base de apoyo más amplia.
- Puede distribuir la carga entre cuatro ruedas.

#### Limitaciones

- Necesita cuatro motores.
- Tiene más componentes y mayor costo.
- En pisos irregulares alguna rueda puede perder contacto.
- Los rodillos no son adecuados para todos los terrenos.

## 4. Robot omnidireccional con ruedas Mecanum

### Construcción

Las ruedas Mecanum tienen rodillos alrededor del perímetro, colocados aproximadamente a 45° respecto al eje de la rueda.

Cuando el motor gira, el contacto de los rodillos con el suelo produce una fuerza con componentes longitudinales y laterales.

### Diferencia respecto a una rueda Omni

En una rueda Omni convencional, los rodillos permiten rodar libremente en la dirección transversal al movimiento motorizado.

En una Mecanum, los rodillos están inclinados. Esto permite obtener componentes laterales aunque las cuatro ruedas principales estén orientadas hacia adelante y atrás.

### ¿Por qué se utilizan cuatro ruedas?

La configuración habitual utiliza cuatro ruedas para combinar sus componentes de fuerza y controlar tres movimientos:

- Avance y retroceso.
- Desplazamiento lateral.
- Giro.

Se utilizan dos ruedas de cada orientación de rodillos y normalmente un motor independiente por rueda [5].

### Orientación respecto al chasis

Los planos de las ruedas principales quedan paralelos a la dirección de avance. Sus ejes quedan transversales al chasis.

En el montaje habitual, al mirar desde arriba, las líneas de los rodillos visibles forman una “X” [5].

### Esquema visto desde arriba

**Frente: ↑**

| Lado izquierdo | Chasis | Lado derecho |
| :---: | :---: | :---: |
| Delantera izquierda: ╲ | Frente ↑ | Delantera derecha: ╱ |
| | Centro ⊙ | |
| Trasera izquierda: ╱ | Parte trasera | Trasera derecha: ╲ |

Los símbolos ╲ y ╱ representan la inclinación de los rodillos vistos desde arriba. Las ruedas principales siguen rodando hacia adelante o atrás.

### Combinación de movimientos

- **Avance:** las cuatro ruedas giran hacia adelante.
- **Retroceso:** las cuatro giran hacia atrás.
- **Izquierda:** las ruedas de una diagonal avanzan y las de la otra retroceden.
- **Derecha:** se invierte la combinación anterior.
- **Diagonal:** se combinan avance y desplazamiento lateral. En una diagonal ideal de 45°, dos ruedas pueden quedar detenidas.
- **Giro:** las ruedas de un lado avanzan y las del otro retroceden.

La combinación precisa depende de la geometría y de la velocidad deseada [6].

### Tabla de sentidos de giro

**Convención:**

- ↑: giro que impulsaría una rueda convencional hacia el frente.
- ↓: giro contrario.
- Las flechas describen el giro de la rueda principal, no el movimiento individual de sus rodillos.
- La tabla corresponde al montaje en “X” mostrado.

| Movimiento | Delantera izquierda | Delantera derecha | Trasera izquierda | Trasera derecha |
| --- | :---: | :---: | :---: | :---: |
| Avanzar | ↑ | ↑ | ↑ | ↑ |
| Retroceder | ↓ | ↓ | ↓ | ↓ |
| Desplazarse a la izquierda | ↓ | ↑ | ↑ | ↓ |
| Desplazarse a la derecha | ↑ | ↓ | ↓ | ↑ |
| Girar a la izquierda | ↓ | ↑ | ↓ | ↑ |
| Girar a la derecha | ↑ | ↓ | ↑ | ↓ |

Para estos movimientos puros se consideran ruedas iguales y velocidades de igual magnitud.

### Ejemplo de movimiento diagonal

Para avanzar hacia la derecha en una diagonal ideal de 45°:

- Delantera izquierda: avanza.
- Delantera derecha: detenida.
- Trasera izquierda: detenida.
- Trasera derecha: avanza.

Las componentes de las dos ruedas activas producen avance y desplazamiento a la derecha.

### Ventajas y limitaciones

**Ventajas:**

- Se desplaza lateralmente sin cambiar su orientación.
- Facilita maniobras en espacios reducidos.
- Combina traslación y giro.

**Limitaciones:**

- Necesita cuatro motores y control coordinado.
- Sus rodillos pueden producir vibraciones.
- Su desempeño depende del contacto con el suelo.
- Puede perder precisión por deslizamiento.

## 5. Robot con dirección Ackermann

### Distribución de las ruedas

La configuración habitual tiene cuatro ruedas convencionales: dos delanteras y dos traseras.

Las ruedas delanteras proporcionan la dirección. La tracción puede estar en las delanteras, las traseras o en las cuatro, según el diseño.

### Diferencia de ángulos durante una curva

En una curva, la rueda interior recorre una trayectoria de menor radio que la exterior. Por eso necesita un ángulo de dirección mayor.

La geometría Ackermann busca que las prolongaciones de los ejes de las ruedas apunten hacia un centro de giro común. Esto reduce el arrastre lateral de los neumáticos [7].

### ¿Qué es el radio de giro?

Es la distancia entre el centro de giro y un punto de referencia del vehículo, como el punto medio del eje trasero.

Debe indicarse qué punto se utiliza porque las distintas partes del vehículo recorren círculos de diferente radio.

### Esquema de una curva hacia la izquierda

**Frente: ↑**

| Exterior izquierdo del vehículo | Lado izquierdo | Centro | Lado derecho |
| :---: | :---: | :---: | :---: |
| | Rueda delantera interior ↖, mayor ángulo | Avance en curva ↖ | Rueda delantera exterior ↖, menor ángulo |
| Centro de giro ⊙ | Rueda trasera interior ↕ | Eje trasero | Rueda trasera exterior ↕ |

El centro de giro se encuentra hacia la izquierda, sobre la prolongación del eje trasero. Las flechas delanteras son simbólicas: ambas ruedas apuntan hacia la curva, pero la interior gira más.

### ¿Por qué no se mueve directamente hacia un costado?

Las ruedas convencionales se oponen a la rodadura transversal y las traseras permanecen orientadas longitudinalmente.

Girar las ruedas delanteras mientras el vehículo está detenido cambia su dirección, pero no desplaza la base. Para cambiar de posición debe avanzar o retroceder describiendo una trayectoria curva.

### Semejanza con un automóvil

Funciona de manera similar a la dirección de un automóvil convencional. Utiliza ruedas directrices para tomar curvas y necesita espacio para maniobrar.

### Ejemplos

- Automóviles autónomos que conservan una dirección convencional.
- Plataformas de investigación de conducción autónoma basadas en vehículos a escala.
- Robots de competencia F1TENTH con dirección tipo automóvil [8].

## 6. Comparación de configuraciones

Las complejidades son relativas para diseños educativos de tamaño semejante.

| Configuración | Número típico de ruedas | Movimiento lateral directo | Giro sobre su eje | Complejidad mecánica | Complejidad de control | Aplicaciones |
| --- | --- | --- | --- | --- | --- | --- |
| Diferencial + castor | 2 motrices y 1 de apoyo | No | Sí | Baja | Baja | Educación y navegación interior. |
| Omni de 3 ruedas | 3 motrices | Sí | Sí | Media | Media | Competencias e investigación. |
| Omni de 4 ruedas | 4 motrices | Sí, con orientación adecuada | Sí | Media | Media-alta | Plataformas de transporte y pruebas. |
| Mecanum | 4 motrices | Sí | Sí | Media | Media-alta | Almacenes y competencias. |
| Ackermann | Normalmente 4 | No | No, en su configuración convencional | Media-alta | Media-alta | Vehículos autónomos tipo automóvil. |

### Selección para diferentes situaciones

| Situación | Configuración elegida | Razón |
| --- | --- | --- |
| Robot pequeño para aprender programación y control. | Diferencial + castor. | Solo necesita coordinar dos motores. |
| Robot dentro de un almacén con espacios reducidos. | Mecanum, si el piso es uniforme. | Permite acercarse lateralmente a estaciones y maniobrar sin orientar primero la base. |
| Plataforma que debe moverse lateralmente sin cambiar su orientación. | Omni de 3 ruedas. | Controla las dos direcciones de traslación y el giro con tres motores. |
| Vehículo autónomo similar a un automóvil. | Ackermann. | Reproduce las maniobras y restricciones de un automóvil. |
| Robot de competencia que cambia rápidamente de dirección. | Omni de 3 ruedas. | Permite cambios de dirección sin girar previamente el chasis. |
| Robot sencillo que utiliza solo dos motores. | Diferencial + castor. | Cada motor controla una rueda y el apoyo no necesita motor. |

## 7. Análisis del movimiento

### Diferencial: giro sobre su propio eje

Las ruedas deben moverse en sentidos opuestos con velocidades iguales en magnitud.

Sus contribuciones al desplazamiento del punto medio se cancelan, mientras que sus contribuciones al giro se suman. Por eso el robot cambia su orientación sin trasladar ese punto.

### Omni: función de los rodillos

Los rodillos giran cuando la rueda se desplaza transversalmente. Así permiten que una rueda sea arrastrada en esa dirección sin bloquear el movimiento.

Al orientar varias ruedas de manera distinta, sus motores aportan componentes de movimiento que pueden combinarse para producir desplazamiento lateral. Los rodillos permiten ese movimiento, pero no lo generan por sí solos.

### Mecanum: movimiento lateral con ruedas paralelas

Los rodillos inclinados producen fuerzas con componentes longitudinales y laterales.

Con la combinación adecuada, las componentes longitudinales se cancelan y las laterales se suman. También se compensan los efectos de giro. El resultado es una traslación lateral del chasis.

### Ackermann: necesidad de avanzar o retroceder

Las ruedas convencionales no permiten rodadura libre hacia sus costados. La dirección delantera orienta la trayectoria, pero no impulsa lateralmente al vehículo detenido.

Para cambiar su posición lateral necesita recorrer curvas hacia adelante o atrás. Así, el desplazamiento lateral se obtiene como resultado de una maniobra.

## 8. Aplicación en un robot real

### TurtleBot3 Burger

| Característica | Descripción |
| --- | --- |
| Nombre | TurtleBot3 Burger. |
| Fabricante | ROBOTIS. |
| Tipo de locomoción | Diferencial con apoyo esférico. |
| Ruedas | Dos ruedas motrices convencionales y un ball caster. |
| Sensores principales | LiDAR de 360°, unidad de medición inercial y encoders de los actuadores. |
| Actuadores de locomoción | Dos actuadores DYNAMIXEL XL430-W250, uno por rueda motriz. |
| Aplicación | Enseñanza, investigación y desarrollo de navegación con ROS. |

El modelo de LiDAR puede variar según la versión del equipo; la documentación del fabricante menciona LDS-01 o LDS-02 [9].

### Imagen

![TurtleBot3 Burger y sus componentes](https://emanual.robotis.com/assets/images/platform/turtlebot3/hardware_setup/turtlebot3_burger_components.png)

**Fuente de la imagen:** manual oficial de ROBOTIS [9].

### ¿Por qué es adecuada esta configuración?

La configuración diferencial facilita el aprendizaje porque utiliza dos motores y permite girar en el lugar.

Los encoders ayudan a estimar el movimiento de las ruedas. El LiDAR proporciona información sobre obstáculos y la IMU ayuda a medir cambios de orientación.

Aunque no puede desplazarse directamente hacia un costado, resulta adecuada para estudiar navegación, localización y planificación de trayectorias en interiores.

## Reflexión final

La configuración diferencial me pareció la más sencilla de comprender porque el movimiento depende principalmente de dos ruedas. Si ambas avanzan igual, el robot sigue recto; si sus velocidades cambian, gira. Esto permite relacionar fácilmente las órdenes de los motores con el movimiento.

Las configuraciones Omni y Mecanum ofrecen mayor libertad de movimiento en el plano porque permiten desplazarse lateralmente y girar sin orientar primero el robot. Sin embargo, requieren coordinar más motores y dependen del buen contacto de sus ruedas con el suelo.

Para construir mi primer robot móvil elegiría una configuración diferencial con rueda de castor. Su estructura es sencilla y me permitiría aprender a controlar motores, leer sensores y evitar obstáculos.

No existe una configuración adecuada para todos los robots porque cada aplicación tiene necesidades diferentes. Es necesario considerar el terreno, la carga, el espacio disponible, el costo y la precisión requerida antes de elegir las ruedas.

## Referencias

Se indica **s. f.** cuando no se identificó una fecha de publicación. Algunas fuentes están en inglés porque corresponden a documentación técnica directa de fabricantes y proyectos de robótica.

1. **WPILib.** **Cinemática de accionamiento diferencial**. 2023.  

   https://docs.wpilib.org/es/2023/docs/software/kinematics-and-odometry/differential-drive-kinematics.html

2. **REV Robotics.** **DUO Omni Wheels**. s. f.  

   https://www.revrobotics.com/DUO-Omni-Wheels/

3. **Ortega Antón, Alberto. Universidad Politécnica de Madrid.** **Algoritmo de control de un robot omnidireccional de tres ruedas**. 2019.  

   https://oa.upm.es/58728/

4. **Proyecto ros2_control.** **omni_wheel_drive_controller**. s. f.  

   https://control.ros.org/master/doc/ros2_controllers/omni_wheel_drive_controller/doc/userdoc.html

5. **REV Robotics.** **Mecanum Wheel Setup and Behavior**. s. f.  

   https://docs.revrobotics.com/duo-build/mecanum-drivetrain-v2/mecanum-wheel-setup-and-behavior

6. **WPILib.** **Cinemática de accionamiento Mecanum**. s. f.  

   https://docs.wpilib.org/es/latest/docs/software/kinematics-and-odometry/mecanum-drive-kinematics.html

7. **Proyecto ros2_control.** **Wheeled Mobile Robot Kinematics**. s. f.  

   https://control.ros.org/master/doc/ros2_controllers/doc/mobile_robot_kinematics.html

8. **Proyecto F1TENTH.** **Presentación del proyecto en ROSCon 2019**. 2019.  

   https://roscon.ros.org/2019/talks/roscon2019_f110th.pdf

9. **ROBOTIS.** **TurtleBot3: Features, Specifications and Components**. s. f.  

   https://emanual.robotis.com/docs/en/platform/turtlebot3/features/
