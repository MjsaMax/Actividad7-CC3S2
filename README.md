### Ejercicios guiados (responde en `README.md`)

#### A) Evitar (o no) `--ff`

* Ejecuta una fusión FF real (ver 1).
* **Pregunta:** ¿Cuándo **evitarías** `--ff` en un equipo y por qué?
```
Como la mayor cantidad de equipos se necesita un historial claro y conciso del repositorio trabajado, es necesario saber el seguimiento de cada rama y cada merge debe ser documentado y ademas como se realiza en equipo, implicaria el avance paralelo del proyecto por lo cual habria conflictos al hacer merge, entonces realizar --ff solo atrasaria al arreglar conflictos entre colaboradores
```

#### B) Trabajo en equipo con `--no-ff`

* Crea dos ramas con cambios paralelos y **fusiónalas con `--no-ff`**.
* **Preguntas:** ¿Qué ventajas de trazabilidad aporta?
```
Aporta al momento de realizar un resumen al momento de crear el merge con un commit.
```
 ¿Qué problemas surgen con **exceso** de merges?
```
Trazabilidad difusa al momento de ver el historial de commits.
```
#### C) Squash con muchos commits

* Haz 3-4 commits en `feature-3` y aplánalos con `--squash`.
* **Preguntas:** ¿Cuándo conviene? 
```
Conviene cuando los commits de una rama son desordenados o poco relevantes para los demas colaboradores.
```
¿Qué se **pierde** respecto a merges estándar?
```
Se pierde trazabilidad respecto a los commits dentro de una rama, es decir squash "resumen" commits.
```
### Conflictos reales con no-fast-forward

**Preguntas**

* ¿Qué pasos adicionales hiciste para resolverlo?
```
Editar el texto innecesario que se formo al momento de realizar el merge. 
```
* ¿Qué prácticas (convenciones, PRs pequeñas, tests) lo evitarían?
```
Que en un proyecto cada colaborador se encargue de partes especificas e independientes y si no fuere asi, entonces comunicacion necesaria entre ellos.
```
### Comparar historiales tras cada método

**Preguntas**

* ¿Cómo se ve el DAG en cada caso?
```
texto desde feat-b.
```
* ¿Qué método prefieres para: trabajo individual, equipo grande, repos con auditoría estricta?
```
texto agregado desde feat-a..sad conflicto en main
```

### Revertir una fusión (solo si **HEAD es un merge commit**)

**Preguntas**

* ¿Cuándo usar `git revert` en vez de `git reset`?
```
Se usa revert para mostrar a los demas colaboradores quien realiza el cambio y por qué, ya que al momento de quitar ramas podria ser un problema para los que estaban desarrollando en esa rama y no existe trazabilidad.
```
* ¿Impacto en un repo compartido con historial público?
```
el impacto es claro, ya que al momento de deshacer un merge o un commit, se pierde información que podría ser util a otros desarrolladores.
```
