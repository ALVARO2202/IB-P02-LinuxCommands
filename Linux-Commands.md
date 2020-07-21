# Práctica 02. Comandos básicos en el Sistema Operativo Linux


### Objetivos
Los objetivos de esta práctica son:

* 1
* 2


### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* Se valorará 
* Se valorará 


**Avise al profesor** al finalizar la realización de cada uno de los pasos que se indican a continuación. No inicie una nueva tarea sin haber revisado la anterior.
### Introducción
El propósito de esta práctica es estudiar los comandos básicos de Linux. 
Con la prevalencia en la actualidad de los sistemas operativos basados en Interfaces Gráficas de Usuario (GUIs), la necesidad 
de interaccionar con el sistema a través de comandos ha disminuído su importancia.
No obstante, hay muchas tareas que son mucho más fáciles de realizar en un entorno Unix usando comandos y el
trabajo mediante comandos también es casi obligatorio en entornos cliente/servidor.
Por otra parte, la familiaridad con Unix mejorará la empleabilidad de cualquier ingeniero en informática.

Si ya está familiarizado con Linux, esta práctica será muy corta. 
Si es Ud. nueva/o en Linux le tomará más tiempo, así que prepárese en consecuencia!

En esta práctica no se va a programar comandos sino que los ejercicios están orientados a conocer los fundamentos del uso de Unix.  
Este conocimiento básico será necesario para completar sus tareas de programación en otras prácticas futuras
de la asignatura.

### Conexión con su VM de la asignatura
En la práctica anterior se estudió cómo realizar la conexión con la máquina virtual que utilizará Ud. en la
asignatura. Recuerde que para ello necesita Ud. un cliente ssh.
* Si se conecta Ud. desde un sistema Linux, abra un terminal y ejecute 
```
ssh usuario@<dirección IP de su máquina>
```
Recuerde que la dirección IP de su máquina tiene un formato similar a `10.6.129.147`
* Si se conecta Ud. desde un sistema Windows, un cliente ssh que le recomendamos es [putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
* Si se conecta Ud. desde un sistema Mac, abra una ventana de terminal (en 'Aplicaciones/utilidades') y
ejecute
```
ssh usuario@<dirección IP de su máquina>
```

Recuerde siempre que si se conecta Ud. desde fuera del campus ULL ha de instalar e iniciar sesión usando un
[cliente VPN](https://www.ull.es/servicios/stic/2016/05/10/servicio-de-vpn-de-la-ull/).

### Comandos Linux
Estudie en [este tutorial](http://linuxcommand.org/index.php)  
al menos hasta el final de la sección 7 (**I/O Redirection**) en el capítulo "Learning the Shell" aunque ¡no le hará daño leer más!.

Pruebe en su máquina virtual los comandos que estudie en el tutorial.

### Ejercicios
1. Cree un subdirectorio `practicas` en su directorio `home` (`~`) y clone (haga una copia) dentro de él del repositorio de esta
práctica en el (sub) directorio `IB-p02-LinuxCommands`.
A este último directorio nos referiremos como 'directorio de trabajo'.
Para ello ejecute:
```
cd ~
mkdir practicas
cd practicas
git clone git@github.com:fsande/IB-P02-LinuxCommands.git IB-p02-LinuxCommands
```

2. Entre en el directorio `IB-p02-LinuxCommands`. 
Encontrará en él el fichero `ProgrammingJoke.txt`. 
¿Cuál es el chiste?.
Busque cualquier otro chiste famoso de programadores y añada el texto del nuevo chiste a continuación de éste.

3. En este momento debería tener un fichero llamado `square.cc` en su directorio de trabajo.
Utilice los comandos que ha aprendido para compilar y ejecutar ese programa.
El programa tiene un error.  
Debería ser capaz de detectar el error después de ejecutar el programa. 
Arregle el error y recompile el programa.
Muestre a quien le evalúe esta práctica el fichero `square.cc` y acredite Ud. que sabe compilar y ejecutar el
programa.

4. ¿Cuál es el comando para borrar un fichero? Por ejemplo, ¿cómo eliminaría el fichero `a.out` resultado de la compilación en el paso anterior?

5. ¿Qué comando usaría para cambiar el nombre de `square.cc` a `numbers-square.cc`?

6. ¿Cómo se muestra un fichero de texto largo para que se detenga en cada pantalla?  
Practique mostrando en pantalla el contenido del fichero `/proc/cpuinfo` que contiene información sobre las CPUs de su
máquina virtual.

7. ¿Qué contiene el fichero de texto `long-text-file.txt` que se encuentra en su directorio de trabajo?

8. ¿Qué hacen las teclas de flechas arriba y flecha abajo cuando está ejecutándose la shell de Linux (bash)?

9. En la shell, escriba el carácter `!` seguido de una letra como la `g` o la `l`, como en `!g` o `!l`. 
Experimente con otras letras después del símbolo de exclamación. ¿Qué hace la exclamación?

10. Experimente con el comando `grep` 
`grep` es un programa que permite buscar texto usando expresiones regulares (estudiará Ud. expresiones regulares más adelante en 2º curso). 
Por ahora, puede usarlo para buscar un patrón de texto.
Un uso básico del comando es: 
```
grep string target-file
```
Ese comando localiza todas las apariciones de la cadena de texto `string` en el fichero `target-file`
El fichero `long-text-file.txt` contiene 187018 palabras.
Use grep para encontrar todas las palabras que contengan "aula" en ese fichero. ¿Cuáles son esas las palabras?

11. Use un *pipe* (encadenamiento de comandos).
El comando `wc` (de *Word Count*) indica cuántas líneas, palabras y caracteres hay en un fichero.
Utilice el comando `man` para conocer el funcionamiento de `wc`, así como información detallada del comando.

Utilice un *pipe* (usando el caracter `|`) para vincular los dos comandos anteriores entre sí, para averiguar 
cuantas veces aparecen en el fichero `long-text-file.txt` cada una de las palabras que contienen la subpalabra "aula".
Escriba un fichero de texto `aula.txt` en el que figure cada una de estas palabras y el número de veces que
aparece en el fichero `long-text-file.txt`.
