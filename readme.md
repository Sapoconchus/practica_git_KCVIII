- ¿Qué comando utilizaste en el paso 11? ¿Por qué? 

> git reset --hard HEAD~1, para volver al anterior commit descartando los cambios del working copy

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? 

> hago "git reflog" para ver el historial de acciones de git y buscar el anterior commit. Copio su identificador (en mi caso 44beac6) y vuelvo a posicionar head (y la rama styled) en él mediante "git reset --had 44beac6"

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

> No. Styled está más "adelante" por lo que ya contenía a master.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 

> Si, porque en cada rama había un git-nuestro.md distinto e incompatible (distinto contenido en las mismas lineas)

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

> No porque es un merge Fastforward y los archivos no están en conflicto.

- ¿Qué comando o comandos utilizaste en el paso 25? 

> git log --graph --decorate --pretty=oneline

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

> Si, porque avanza un commit solamente. Es decir, los commits anteriores siguen estando accesibles

- ¿Qué comando o comandos utilizaste en el paso 27?

> git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?

> "git status" para ver el working copy y "git checkout -- git-nuestro.md"

- ¿Qué comando o comandos utilizaste en el paso 29?

> git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?

> voy al último commit en el que estaba title antes de borrarla (lo veo en el mensaje que devuelve tras eliminar title en el paso anterior, pero podría localizarse igualmente con un reflog) Estamos en "detached Head". Creamos la rama title para que quede el puntero en ese commit y nos movemos a la rama master con "git checkout master". Desde ahí volvemos a hacer el merge con title con "git merge title". Y así queda el merge rehecho

- ¿Qué comando o comandos usaste en el paso 32?

> Uso "git log" para ver el grafo. Localizo el commit incial, en mi caso el "aa37342". Hago "git reset --hard aa37342" y ya estoy en el commit inicial. Uso el "--hard" para que me modifique también el working copy y estar en la situación incial.

- ¿Qué comando o comandos usaste en el punto 33?

> "git reflog" para localizar el commit (en mi caso el e114388) y "git reset --hard e114388" para volver al commit final.




