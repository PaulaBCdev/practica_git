- ¿Qué comando utilizaste en el paso 11?¿Por qué?
  git reset --hard HEAD~1
  Porque había que borrar el último commit (HEAD~1 para ir al commit anterior), borrando las modificaciones del Working Copy (--hard para borrar el contenido del commit).

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
  Primero usé git log para comprobar que, efectivamente, después del paso 11 tenia solo un commit (el primero que hice en main).

  Después use git reflog para ver lo que ha pasado en el repo hasta ese momento (los cambios de rama, commits, resets, etc).
  Aquí busqué el commit al que quería volver y copié su identificador.

  Por ultimo, hice git reset --hard <identificador_del_commit> para volver al commit que quería y que todo volviese a estar como estaba cuando lo subi al repo. 

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
  No causó ningún conflicto porque la rama styled ya tenía el unico commit que tenía main, así que no hubo cambios.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
  Sí causó conflicto porque modifiqué en ambas ramas el archivo git-nuestro.md, en las mismas lineas.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
  No hubo ningún conflicto porque no había archivos en ambas ramas que se hubiesen cambiado en las mismas líneas, como sí ocurrió al mergear htmlify en styled.

- ¿Qué comando o comandos utilizaste en el paso 25?
  git log --graph

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
  Sí podría ser fast-forward porque era una lista de commits, por lo que main podría haber absorbido a title sin tener necesidad de crear un nuevo commit.

- ¿Qué comando o comandos utilizaste en el paso 27?
  git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
  git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
  git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?
  git reset --hard <identificador del commit donde está el merge>

- ¿Qué comando o comandos usaste en el paso 32?
  git reflog para ver el identificador del commit al que quiero ir.
  git checkout <identificados del commit> para ir a ese commit.

- ¿Qué comando o comandos usaste en el punto 33?
  git reflog para copiar el identificador del commit al que quiero ir.
  git checkout <identificador del commit> para ir al commit.

