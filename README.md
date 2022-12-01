6. Clonamos el proyecto dentro de **Ordenador2** y lo abrimos.

7. Creamos una nueva funcionalidad, para lo cual creamos una rama "feat_persona" y la desarrollamos (ver mi log de commits). Una vez lista subimos la rama (```git push feat_persona```). Después, nos movemos a master para hacer un merge de "feat_persona" **localmente**. Al no haber nuevos commits en master, el merge debería ser automático y sin conflictos.
7. Creamos una nueva funcionalidad, para lo cual creamos una rama "feat_persona" y la desarrollamos (ver mi log de commits). Una vez lista subimos la rama (```git push feat_persona```). Después, nos movemos a master para hacer un merge de "feat_persona" **localmente**. Al no haber nuevos commits en master, el merge debería ser automático y sin conflictos. Después del merge, hacemos un push de master con los nuevos cambios añadidos.

8. Volvemos a **Ordenador1**. Recordamos el estado de nuestro proyecto en este ordenador haciendo un ```git status``` y un ```git log```. Si no nos indica que el master local está por detrás del remoto (origin/master), será necesario hacer un ```git fetch```.

@@ -62,14 +62,14 @@

    9. Terminamos el merge con add y commit, y hacemos un push.

12. Volvemos a Ordenador2 y comprobamos si tenemos todo al día con ```git status``` y ```git log```. Si no nos indica que el master local está por detrás del remoto, será necesario hacer un ```git fetch```, que ahora nos indicará que debemos hacer un pull.
11. Volvemos a Ordenador2 y comprobamos si tenemos todo al día con ```git status``` y ```git log```. Si no nos indica que el master local está por detrás del remoto, será necesario hacer un ```git fetch```, que ahora nos indicará que debemos hacer un pull.

13. Ahora vamos a simular cómo se desarrollaría en paralelo en varias ramas (distintas personas). No crearemos carpetas que simulen ordenadores pero cada rama representará el trabajo independiente de cada componente del equipo de trabajo.
12. Ahora vamos a simular cómo se desarrollaría en paralelo en varias ramas (distintas personas). No crearemos carpetas que simulen ordenadores pero cada rama representará el trabajo independiente de cada componente del equipo de trabajo.

    1. Creamos una rama "feat_inmutable_fields" para evitar que se pueda cambiar el nombre y la fecha de contratación de un empleado (asumimos que las especificaciones del proyecto lo impiden, sea o no razonable).
    1. Creamos dos ramas desde master, que desarrollaremos sin hacer merge a master (simulando otro desarrollador trabajando en paralelo): 
        1. "feat_inmutable_fields" para evitar que se pueda cambiar el nombre y la fecha de contratación de un empleado (asumimos que las especificaciones del proyecto lo impiden, sea o no razonable).
        2. "bug_edad_negativa", para garantizar que la edad de un empleado no pueda ser negativa.

    2. Sin hacer push (simulando otro desarrollador trabajando en paralelo), creamos otra rama bug_edad_negativa, para garantizar que la edad de un empleado no pueda ser negativa.
    3. Una vez desarrolladas, hacemos el merge de ambas ramas a master solventando conflictos.

    3. Hacemos merge de ambas ramas a master solventando conflictos.

14. Realizamos otras mejoras en la rama feat_deprecated_data_type para solucionar los problemas de la librería obsoleta java.util.Date, y los mergeamos.
13. Realizamos otras mejoras en la rama feat_deprecated_data_type para solucionar los problemas de la librería obsoleta java.util.Date, y los mergeamos.