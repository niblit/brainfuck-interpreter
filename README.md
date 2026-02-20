# brainfuck-interpreter


El lenguaje consta de ocho comandos. Un programa Brainfuck es una secuencia de estos comandos. Los comandos se ejecutan secuencialmente, con algunas excepciones: un puntero de instrucción comienza en el primer comando, y cada comando al que apunta se ejecuta, tras lo cual normalmente avanza al siguiente comando. El programa termina cuando el puntero de instrucción pasa del último comando.

En el modelo abstracto canónico de máquina para Brainfuck, un programa opera sobre una cinta unidimensional de celdas de memoria indexadas desde cero y sin límites a la derecha. Cada celda contiene un entero sin signo de 8 bits (0–255) y se inicializa a cero. La aritmética en celdas se envuelve módulo 256, por lo que incrementar 255 produce 0 y decrementar 0 produce 255. Un puntero de datos (inicializado para apuntar al byte más a la izquierda del array) indica la celda actual en la cinta y puede moverse a la izquierda o a la derecha. Moverse a la izquierda desde la primera celda (índice 0) no está definido. El lenguaje proporciona ocho comandos que modifican la cinta, mueven el puntero, realizan entrada/salida (usando la codificación de caracteres ASCII) o bucles de control.

Los ocho comandos del idioma consisten cada uno en un solo carácter:

| Carácter | Instrucción realizada |
| ----------- | ----------- |
| Carácter | Instrucción realizada |
