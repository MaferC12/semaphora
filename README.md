# semaphora

P_ini.c
Programa inicial que configura los recursos necesarios para la comunicación entre procesos, se crea la semaphora con clave única, escribe un mensaje inicial en la memoria compartida escribe la cadena "003holaUCSP". El programa entra en un bucle while que espera hasta que el contenido de la memoria compartida sea una cadena vacía. 

P_print.c
Obtiene el identificador del segmento de memoria compartida, adjunta el segmento de memoria compartida al espacio de direcciones del proceso. Copia el contenido de la memoria compartida en un buffer local y lo imprime el contenido en la consola, permitiendo observar en tiempo real los cambios realizados por otros procesos.

Px.c
Verifica que el programa reciba exactamente un argumento, que en este caso debe ser un entero. Convierte el argumento recibido a un entero v. Obtiene el identificador del semáforo existente utilizando SEM_KEY y obtiene el identificador del segmento de memoria compartida existente utilizando SHM_KEY. También entra en un bucle infinito donde realiza: Realiza la operacion P(wait) donde ejecuta semop para decrementar el semáforo y asegurar acceso exclusivo a la memoria compartida.
Convierte los primeros tres caracteres de la memoria compartida a un entero(shared_val) utilizando atoi. Comprueba si shared_val es igual a v - 1, si es así construye una nueva cadena, formateando v como un entero de tres dígitos seguido de holapx y el valor original v_aux.
Escribe esta cadena en la memoria compartida.Incrementa v en 3. 
En conclusión, este programa modifica el contenido de la memoria compartida, asegurando que solo un proceso acceda a la memoria a la vez.

