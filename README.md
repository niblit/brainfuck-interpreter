# brainfuck-interpreter


El lenguaje consta de ocho comandos. Un programa Brainfuck es una secuencia de estos comandos. Los comandos se ejecutan secuencialmente, con algunas excepciones: un puntero de instrucción comienza en el primer comando, y cada comando al que apunta se ejecuta, tras lo cual normalmente avanza al siguiente comando. El programa termina cuando el puntero de instrucción pasa del último comando.

En el modelo abstracto canónico de máquina para Brainfuck, un programa opera sobre una cinta unidimensional de celdas de memoria indexadas desde cero y sin límites a la derecha. Cada celda contiene un entero sin signo de 8 bits (0–255) y se inicializa a cero. La aritmética en celdas se envuelve módulo 256, por lo que incrementar 255 produce 0 y decrementar 0 produce 255. Un puntero de datos (inicializado para apuntar al byte más a la izquierda del array) indica la celda actual en la cinta y puede moverse a la izquierda o a la derecha. Moverse a la izquierda desde la primera celda (índice 0) no está definido. El lenguaje proporciona ocho comandos que modifican la cinta, mueven el puntero, realizan entrada/salida (usando la codificación de caracteres ASCII) o bucles de control.

Los ocho comandos del idioma consisten cada uno en un solo carácter:

| Carácter | Instrucción realizada |
| ----------- | ----------- |
| > | Incrementa el puntero de datos en uno (para apuntar a la siguiente celda a la derecha). |
| < | Disminuir el puntero de datos en uno (para que apunte a la siguiente celda a la izquierda). Indefinido si está en 0. |
| + | Incrementa el byte en el puntero de datos en uno módulo 256. |
| - | Disminuye el byte en el puntero de datos en uno módulo 256. |
| . | Saca el byte en el puntero de datos. |
| , | Acepta un byte de entrada, almacenando su valor en el byte del puntero de datos. |
| [ | Si el byte en el puntero de datos es cero, en lugar de mover el puntero de instrucción hacia adelante al siguiente comando, salta hacia adelante al comando después del comando correspondiente. ] |
| ] | Si el byte en el puntero de datos es distinto de cero, en lugar de mover el puntero de instrucción hacia adelante al siguiente comando, salta de nuevo al comando después del comando correspondiente. [ |
