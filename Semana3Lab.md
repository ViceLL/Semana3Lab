Vicente Vargas
1097813
Programacion II
0. URL del repositorio de github.com

1. ¿Cómo sabemos si un programa o script terminó de manera exitosa desde el shell / consola?
Sabemos que se ejecutó con éxito cuando al ejecutarlo nos notifica la terminal que el archivo se puede ejecutar para luego correr el código y si tiene algún error lo notificará cuando lo vaya a compilar y no se ejecutará. 

2. Cree un script que escriba "Hola <nombre>.". https://www.youtube.com/watch?v=CmlCC1NPEGk&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=1
El script debe recibir el nombre como argumento de línea de comando. Si el usuario digita algún nombre el script escribe al STDOUT el mensaje indicado y termina retornando exitosamente (return code apropiado). Si el usuario no digita ningún nombre entonces el script termina con error (return code 100). No usar ningún lenguaje de programación compilado o interpretado sólo el propio scripting language. El vídeo debe evidenciar los dos casos: salida exitosa y salida de error.

3. Cree un script similar al del punto 2 pero la lógica debe implementarse en un lenguaje de programación (no scripting).
https://www.youtube.com/watch?v=JnA1Bty2_S4&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=2
Ejemplo desde un script de bash (windows), puede invocar un programa creado previamente en lenguaje C. El Script debe transferir el parámetro con el nombre a saludar. El script debe devolver el mismo código de retorno del programa.


4. ¿Qué es el redireccionamiento en el contexto de la ejecución de un programa, script o comando de consola?
Una redirección consiste en trasladar la información de un tipo a otro. Un ejemplo podría ser de la salida estándar a la entrada estándar o del error estándar a la salida estándar.
5. ¿Cuáles números o constantes representan los streams de I/O clásicos (Standard Input, Standard Output y Standard Error) en los siguientes sistemas operativos: Unix/Linux, MacOS y Windows?
Valor entero
Nombre
0
Entrada estándar (stdin)
1
Salida estándar (stdout)
2
Error estándar (stderr)

6. Cree un programa que reciba un número como argumento de línea de comando, si el número es negativo o cero debe escribir por el Standard Error el mensaje "Invalid input <numero>.". Si el número es positivo, debe escribir por el Standard Output el mensaje "Good one <numero>.".
https://www.youtube.com/watch?v=tu1Z6SnYaVw&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=3

7. Desde la consola corra el programa 6, redireccionando el Standard Output a un archivo de nombre out.txt, corra el programa con valores positivos, negativos y cero.
https://www.youtube.com/watch?v=S-4jJeqU86s&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=4
Muestre el contenido del archivo, desde la consola, con cada ejecución, para confirmar que sólo contiene el mensaje cuando prueba con un valor positivo. Pruebe con más de un valor positivo.

8. Desde la consola corra el programa 6, redireccionando el Standard Error a un archivo de nombre err.txt, corra el programa con valores positivos, negativos y cero.
https://www.youtube.com/watch?v=Sm7idAPm1Ww&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=5
Muestre el contenido del archivo, desde la consola, al con cada ejecución, para confirmar que solo contiene el mensaje cuando prueba con valores negativos o cero. Pruebe con mas de un valor invalido.

9. Cree un programa similar al 6, pero que reciba su entrada desde el Standard Input, no desde los argumentos de linea de comando.
https://www.youtube.com/watch?v=kM0DrhBH6aA&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=6

10. ¿Qué es el Piping en Unix y Linux, para qué sirve? de algunos ejemplos? Referencia: https://www.geeksforgeeks.org/piping-in-unix-or-linux/
Método de redirección utilizada en Linux y otros sistemas operativos similares a Unix para enviar la salida de un comando para su posterior procesamiento . Los sistemas Linux o Unix dejan que la salida estándar de un comando se conecte a la salida estándar de otro comando. Esto se puede hacer usando la barra vertical '|' .


11. Cree un programa que escriba al Std. Out los números del 1 hasta N.
https://www.youtube.com/watch?v=B37O10qtavA&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=7
N sera un número capturado como argumento de línea de comando. Ejemplo: ($ simboliza el prompt)
$ Contador.exe 3
$
Note que hay una línea vacía entre el último número y el prompt. Esto quiere decir que el programa debe imprimir una línea en blanco antes de terminar. Si la entrada no es un número positivo entero, el programa debe imprimir un error por el Std. Error. Ejemplo:
$ Contador.exe Tres
Invalid input Tres.
$ Note que sigue habiendo una línea en blanco antes de salir, y recuerde que ese mensaje fue enviado al Std. Error no al Std. Output.

12. Cree un programa que reciba números desde el Std. Input hasta recibir una linea en blanco, vacía, para luego escribir al Std. Output la sumatoria de los valores.
https://www.youtube.com/watch?v=Q5Aa42QKhSQ&list=PLoLev3p8EawBQnp9oAWFVUkMWWzaidUQN&index=8
Ejemplo (std-in), (std-out) y (std-err) representan la fuente y salidas de cada línea según aplique.
$ Sum.exe
1 (std-in)
2 (std-in)
3 (std-in)
(std-in)
6 (std-out)
(std-out)
$
En este ejemplo el usuario invoco el programa y luego escribió los números 1, 2 y 3 en cada línea (presionando Enter luego de cada uno). Luego para señalar que desea terminar y obtener la sumatoria dejo una linea en blanco (solo presionando Enter), luego el programa escribió al Std. Out. la sumatoria de los valores (6), y antes de salir dejo la linea en blanco mandatoria.
Si el programa recibe una entrada que no es un número entero debe escribir un mensaje de error al Std. Error. Ejemplo:
$ Sum.exe
1 (std-in)
Hola mundo cruel (std-in)
Invalid input "Hola mundo cruel" (std-err)
3 (std-in)
(std-in)
4 (std-out)
(std-out)
$

13. Cree un programa similar al 12, pero en lugar de sumar debe escribir al Std. Out el cuadrado de los números recibidos.
Ejemplo:
$ Square.exe
1 (std-in)
1 (std-out)
2 (std-in)
4 (std-out)
Hola mundo cruel (std-in)
Invalid input "Hola mundo cruel" (std-err)
3 (std-in)
9 (std-out)
$
14. Combine, desde el shell y utilizando piping, los 3 programas para obtener la sumatoria del cuadrado de los números de 1 a N.
Ejemplo (con N=10):
$ Counter.exe 10 | Square.exe | Sum.exe
385 (std-out)
(std-out)
$

15. Ponga los tres programas disponibles en cualquier lugar del shell, agregándolos a la variable PATH. Demuestre que puede invocarlos desde cualquier lugar en el shell, y no solo desde la ruta donde están guardados.

16. Cree un script para combinar los tres programas utilizando piping.
Ejemplo:
$ SumOfSquares.bat 10
385 (std-out)
(std-out)
$

17. Ponga disponible el script desde cualquier lugar en el shell, agregándolo al PATH. Demuestre que puede ejecutarlo desde cualquier lugar, no solamente desde donde está guardado.
