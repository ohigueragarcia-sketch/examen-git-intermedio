# Examen Git – Nivel Intermedio

Este examen evalúa el dominio práctico de **Git** mediante la realización de una serie de tareas sobre un repositorio real.

Lee atentamente  **todo el documento antes de comenzar** y sigue las instrucciones en el orden indicado.

---

## Normas generales

- El examen se realiza **exclusivamente mediante comandos Git** (no interfaz gráfica). Se recomienda el uso de la herramienta GIT Bash que tenéis instalada en todos los ordenadores del aula.
- Todas las tareas deben realizarse sobre el repositorio proporcionado.
- **No se permite borrar ni reescribir el historial** salvo cuando el enunciado lo indique explícitamente.
- **No se debe trabajar directamente sobre la rama `main`**, salvo cuando el ejercicio lo indique.
- No se debe modificar el archivo `.gitignore` salvo que un hito lo indique de forma expresa.
- Cada hito debe generar **evidencias obligatorias** para su evaluación.
- Las evidencias deben ser **salidas reales del sistema** (no texto escrito por el alumno).
- Antes de continuar con un nuevo hito, asegúrate de que tu repositorio está en un estado coherente.

---

## Mensajes de commit

Todos los commits deben incluir un mensaje con el siguiente formato obligatorio:

NOMBRE_APELLIDO: mensaje claro y descriptivo


Ejemplo:
Juan Pérez: Crear carpeta personal y notas iniciales


- El mensaje debe ser **atómico**, **descriptivo** y **claro**.
- Los commits con mensajes genéricos o sin el formato indicado podrán ser penalizados.

---

## Carpeta personal

En algún momento del examen vas a tener que crear una carpeta personal dentro de la carpeta `/alumnos`. Utiliza la siguiente nomenclatura:
`APELLIDO1_NOMBRE`
En mayúsculas, sin tildes, sin espacios ni guiones, sólo el guión bajo '_' de separación entre apellido y nombre. 

> ⚠️ Aviso  
> El enunciado de la práctica se refiere a esta carpeta como `TU_NOMBRE`


---

## Evidencias de evaluación

Cada hito indica qué evidencias deben entregarse.

### Tipos de evidencias válidas
- **Archivos `.log`** generados a partir de comandos Git.
- **Capturas de pantalla** (`.png` o `.jpg`) donde se vea claramente el resultado solicitado.

### Importante
- No se aceptan explicaciones escritas por el alumno.
- No se aceptan listados de comandos ejecutados.
- Las evidencias deben ser **generadas por el sistema**.
- Los nombres de los archivos de evidencia deben coincidir **exactamente** con lo indicado en cada hito.

---

## Consejos

- Se recomienda usar el comando  
  `git log --oneline --graph --all`  
  para comprobar el estado del historial antes de continuar con el siguiente hito.
- Lee cada hito completo antes de ejecutarlo.
- No avances si no has completado correctamente el hito anterior.

---
---

# Bloque 1: Configuración y estructura

## 1️⃣ Hito 1 – Identidad y clonado del repositorio

### 🎯 Objetivo
Configurar correctamente tu identidad en Git **a nivel local** y clonar el repositorio del examen en tu equipo.



### 📋 Instrucciones

1. Crea en tu equipo la carpeta examenGIT.
2. Clona el repositorio del examen en la carpeta.
3. Dentro de la carpeta `/alumnos`, crea la carpeta `TU_NOMBRE`.
4. Configura tu nombre de usuario en Git **solo para este repositorio**.
5. Configura tu correo electrónico en Git **solo para este repositorio**.
6. Comprueba que la identidad configurada es correcta.

> ⚠️ Aviso  
> No se permite configurar la identidad de Git a nivel global (`--global`).



### 🔍 Evidencias obligatorias

Debes generar **un único archivo de evidencia**, dentro de tu carpeta personal.

- **Archivo:** `alumnos/TU_NOMBRE/log_hito1.log`
- **Contenido:**  
  La salida de un comando de Git que muestra que la identidad configurada (nombre de usuario y correo electrónico) es correcta.

Para generar la evidencia:
1. Ejecuta el comando de Git que permite comprobar la identidad configurada.
2. Redirige la salida de ese comando al archivo de evidencias.

Ejemplo:
```bash
comando_git > alumnos/TU_NOMBRE/log_hito1.log
```


### ✅ Criterios de evaluación

- La identidad (`user.name` y `user.email`) está configurada **a nivel local**.
- El repositorio ha sido clonado correctamente.
- Los archivos de evidencia existen, tienen el nombre correcto y contienen información válida.

---

---

## 2️⃣ Hito 2 – Espacio de trabajo y primer commit

### 🎯 Objetivo
Crear tu espacio personal de trabajo dentro del repositorio y realizar tu **primer commit correctamente identificado**.



### 📋 Instrucciones

1. Accede a tu carpeta personal dentro de `/alumnos/TU_NOMBRE`.
2. Crea un archivo llamado `notas.md`.
3. Escribe una breve línea de texto dentro del archivo (contenido libre).
4. Comprueba el estado del repositorio.
5. Añade el archivo al área de preparación (staging).
6. Realiza un commit siguiendo **obligatoriamente** el formato de mensaje indicado en las normas generales.



### 🔍 Evidencias obligatorias

Debes generar **un único archivo de evidencia**, dentro de tu carpeta personal.

- **Archivo:** `alumnos/TU_NOMBRE/log_hito2.log`
- **Contenido:**  
  La salida de un comando de Git que muestre:
  - que el archivo `notas.md` ha sido confirmado (commit),
  - el mensaje del commit realizado.

Para generar la evidencia:
1. Ejecuta el comando de Git que permite ver el historial de commits.
2. Redirige la salida de ese comando al archivo de evidencias.

Ejemplo:
```bash
comando_git > alumnos/TU_NOMBRE/log_hito2.log
```

### ✅ Criterios de evaluación

- El archivo notas.md existe dentro de la carpeta del alumno.
- El archivo ha sido añadido y confirmado correctamente.
- El commit tiene un mensaje con el formato:
    NOMBRE_APELLIDO: mensaje claro y descriptivo

---

---
## 3️⃣ Hito 3 – El archivo invisible

### 🎯 **Objetivo**  
Comprobar que Git ignora correctamente un archivo **nuevo** según las reglas del `.gitignore` y conseguir que dicho archivo pase a ser seguido por Git **sin modificar ni eliminar el archivo `.gitignore`**.

### 📋 **Instrucciones**

1. Accede a tu carpeta personal dentro de `/alumnos/TU_NOMBRE`.
2. Crea un archivo nuevo llamado `meIgnoras.txt`.
3. Escribe dentro una línea de texto (contenido libre).
4. Guarda el archivo.
5. Comprueba el estado del repositorio y verifica que el archivo está siendo ignorado por Git.
6. Recoge la evidencia del punto 5 (ver **Evidencias obligatorias** más abajo)
7. Sin modificar ni eliminar el archivo `.gitignore`, consigue que el archivo `meIgnoras.txt` deje de ser ignorado y pase a ser seguido por Git.
8. Realiza un commit con el formato de mensaje indicado en las normas generales.

### 🔍 **Evidencias obligatorias**

Debes generar **dos archivos de evidencia**, dentro de tu carpeta personal.

#### Evidencia 1 – Archivo ignorado

- **Archivo:** `alumnos/TU_NOMBRE/log_hito3_1.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que el archivo `meIgnoras.txt` **está siendo ignorado** por Git.

Para generar la evidencia ejecuta el comando de Git correspondiente y redirige su salida al archivo de evidencias.
Ejemplo:
```bash
comando_git > alumnos/TU_NOMBRE/log_hito3_1.log
```

#### Evidencia 2 – Archivo seguido por Git

- **Archivo:** `alumnos/TU_NOMBRE/log_hito3_2.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que el archivo `meIgnoras.txt` ya no está ignorado, está siendo seguido por Git, y forma parte de un commit.

Para generar la evidencia ejecuta el comando de Git correspondiente y redirige su salida al archivo de evidencias.
Ejemplo:
```bash
comando_git > alumnos/TU_NOMBRE/log_hito3_2.log
```


✅ **Criterios de evaluación**

- El archivo `meIgnoras.txt` es un archivo nuevo.
- El archivo se crea dentro de la carpeta personal del alumno.
- Inicialmente, el archivo está correctamente ignorado por Git.
- El archivo pasa a ser seguido por Git sin modificar ni eliminar `.gitignore`.
- Existe un commit que incluye el archivo.
- Las dos evidencias existen, tienen el nombre correcto y contienen salidas reales de Git.

---

---
## 4️⃣ Hito 4 – Nueva funcionalidad (rama)

### 🎯 **Objetivo**  
Crear una rama nueva y realizar un cambio en el proyecto desde esa rama.

### 📋 **Instrucciones**

1. Crea una rama llamada `feature-log`.
2. Cambia a la rama `feature-log`.
3. Abre el archivo `examen.py`.
4. Añade una línea nueva que muestre tu nombre completo por pantalla (un `print` con tu nombre) y guarda los cambios.
5. Comprueba el estado del repositorio.
6. Añade el cambio al área de preparación (staging).
7. Realiza un commit con el formato de mensaje indicado en las normas generales.

### 🔍 **Evidencias obligatorias**

Debes generar **un archivo de evidencia**, dentro de tu carpeta personal.

- **Archivo:** `alumnos/TU_NOMBRE/log_hito4.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que:
  - estás en la rama `feature-log`,
  - existe un commit en esa rama con tu cambio en `examen.py`.

Para generar la evidencia ejecuta el comando de Git correspondiente y redirige su salida al archivo de evidencias.
Ejemplo:
```bash
comando_git > alumnos/TU_NOMBRE/log_hito4.log
```

### ✅ **Criterios de evaluación**

- La rama `feature-log` existe y el alumno trabaja sobre ella.
- `examen.py` contiene el `print` añadido con el nombre completo del alumno.
- El commit se ha realizado en `feature-log` y tiene un mensaje correcto.
- El archivo `log_hito4.log` existe y contiene una salida real de Git.

---
---
## 5️⃣ Hito 5 – Pausa de emergencia (stash)

### 🎯 Objetivo  
Guardar cambios sin commit usando `stash`, comprobar que `main` está limpia y recuperar después el trabajo en tu rama.

### 📋 Instrucciones

1. Asegúrate de estar en tu rama `feature-log`.
2. Modifica el archivo `examen.py` (haz un cambio pequeño y fácil de reconocer).
3. **No hagas commit**.
4. Guarda tus cambios en el stash.
5. Cambia a la rama `main`.
6. Comprueba que en `main` no hay cambios pendientes (rama limpia).
7. Vuelve a la rama `feature-log`.
8. Recupera los cambios desde el stash.
9. Comprueba que el cambio vuelve a estar presente en tu copia de trabajo.

### 🔍 Evidencias obligatorias

Debes generar **dos evidencias** dentro de tu carpeta personal:

1. **Archivo:** `alumnos/TU_NOMBRE/log_hito5_1.log`  
   **Contenido:** salida de Git que demuestre que existe al menos un elemento guardado en el stash.

2. **Archivo:** `alumnos/TU_NOMBRE/log_hito5_2.png`  (o `.jpg`)
- **Contenido:**  Una única captura donde se vea claramente, en la misma terminal:
  - que estamos en la rama `main` y se encuentra limpia,
  - el cambio de vuelta a la rama `feature-log`,
  - la recuperación del trabajo desde el stash,
  - y la existencia de cambios en el directorio de trabajo.

### ✅ Criterios de evaluación

- El alumno guarda cambios en el stash sin hacer commit.
- El alumno cambia a `main` y demuestra que está limpia.
- El alumno vuelve a `feature-log` y recupera correctamente el trabajo.
- Las evidencias existen, tienen el nombre correcto y contienen salidas reales de Git.

---
---

## 6️⃣ Hito 6 – Conflicto en la lista (remoto)

### 🎯 Objetivo  
Resolver un **conflicto de mezcla (merge)** provocado intencionadamente por una modificación previa en el repositorio remoto.

### 📋 Instrucciones

1. Asegúrate de estar en la rama `main`.
2. Abre el archivo `lista_clase.md`.
3. Localiza tu **apellido** en la lista (los apellidos están sin vocales por privacidad).
4. Modifica **solo tu línea**, sustituyendo `Nombre` por tu nombre real.
5. Guarda el archivo.
6. Añade el cambio al área de preparación (staging).
7. Realiza un commit con el formato de mensaje indicado en las normas generales.
8. Sincroniza tu repositorio local con el remoto.
9. Durante la sincronización aparecerá un **conflicto** en `lista_clase.md`.
10. Recoge la evidencia del conflicto anterior (ver **Evidencias obligatorias** más abajo)
11. Resuelve el conflicto **manualmente**, dejando tu línea correcta y sin perder los cambios del remoto.
12. Finaliza la mezcla (merge) y deja el repositorio en un estado limpio.

> ⚠️ Aviso  
> El conflicto que aparece en este hito ha sido **provocado intencionadamente** por el profesor.  
> Es normal que ocurra. Debes resolverlo y continuar.

### 🔍 Evidencias obligatorias

Debes generar **dos evidencias** dentro de tu carpeta personal.

#### Evidencia 1 – Conflicto detectado

- **Archivo:** `alumnos/TU_NOMBRE/log_hito6_1.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que existe un conflicto pendiente de resolver en el repositorio (archivo en estado “unmerged”).

#### Evidencia 2 – Conflicto resuelto

- **Archivo:** `alumnos/TU_NOMBRE/log_hito6_2.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que:
  - el conflicto ha sido resuelto,
  - la mezcla se ha completado correctamente,
  - y el repositorio vuelve a estar en un estado limpio.

### ✅ Criterios de evaluación

- El alumno modifica únicamente su línea en `lista_clase.md`.
- El conflicto aparece al sincronizar con el remoto.
- El conflicto se resuelve **manualmente** (no abortado).
- La línea del alumno queda con el formato correcto (`APELLIDO Nombre`).
- La mezcla se completa con éxito y el repositorio queda limpio.
- Las evidencias existen, tienen el nombre correcto y contienen salidas reales de Git.

---
---
## 7️⃣ Hito 7 – Enmienda de un commit

### 🎯 Objetivo  
Modificar el **mensaje del último commit** realizando una enmienda, **sin crear un nuevo commit**.

### 📋 Instrucciones

1. Localiza el **último commit** realizado en tu repositorio.
2. Guarda una evidencia del mensaje actual de ese commit.
3. Utiliza el comando de Git adecuado para **cambiar el mensaje del último commit**.
4. Sustituye el mensaje original por uno más claro y profesional (por ejemplo: `feat: corregir lista de clase`).
5. Guarda una evidencia del estado final del commit.
6. Comprueba que **no se ha creado un nuevo commit**.

> ⚠️ Aviso  
> Este hito reescribe el historial. Es una operación permitida **solo porque el commit aún no ha sido compartido**.

### 🔍 Evidencias obligatorias

Debes generar **un único archivo de evidencia**, dentro de tu carpeta personal.

- **Archivo:** `alumnos/TU_NOMBRE/log_hito7.log`
- **Contenido:**  
  La salida del comando de Git **antes y después** de la enmienda, de forma que se pueda comprobar el cambio de mensaje.

- Al recoger la primera evidencia creamos el archivo de evidencias.
  ``` bash 
      comando git > log_hito7.log ```
- En la segunda lo modificamos añadiendo la segunda evidencia en el mismo archivo.
  ``` bash
      otro_comando git >> log_hito7.log ```

### ✅ Criterios de evaluación

- Existe evidencia del mensaje **antes** de la enmienda.
- Existe evidencia del mensaje **después** de la enmienda.
- No se ha creado un nuevo commit.
- El mensaje final es claro y profesional.
- El archivo `log_hito7.log` contiene salidas reales de Git.

---
---
## 8️⃣ Hito 8 – Conflicto local entre ramas

### 🎯 Objetivo  
Provocar y resolver un **conflicto local** al fusionar dos ramas que modifican **exactamente la misma línea del mismo archivo**, decidiendo conscientemente con qué versión quedarse.

### 📋 Instrucciones

1. Asegúrate de tener dos ramas en tu repositorio: `main` y `feature-log`.
2. Cambia a la rama `main`.
3. En la carpeta `/assets`, abre el **único archivo existente**.
4. Localiza una línea concreta del archivo (elige una cualquiera).
5. Modifica esa línea con un cambio sencillo y fácil de reconocer.
6. Guarda el archivo y realiza un commit.
7. Cambia a la rama `feature-log`.
8. Modifica **exactamente la misma línea del archivo que modificaste en `main`**,  
   pero con un contenido diferente.
9. Guarda el archivo y realiza un commit.
10. Desde la rama `feature-log`, intenta fusionar (`merge`) la rama `main`.
11. Aparecerá un **conflicto local**.
12. Resuelve el conflicto manualmente, decidiendo con qué versión quedarte.
13. Finaliza la mezcla y deja el repositorio en un estado limpio.

> ⚠️ Aviso  
> Este conflicto es **local y controlado**.  
> No interviene el repositorio remoto ni otros compañeros.

### 🔍 Evidencias obligatorias

Debes generar **dos evidencias**, dentro de tu carpeta personal.

#### Evidencia 1 – Conflicto local detectado

- **Archivo:** `alumnos/TU_NOMBRE/log_hito8_1.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que existe un conflicto local pendiente de resolver tras intentar la fusión.

#### Evidencia 2 – Conflicto local resuelto

- **Archivo:** `alumnos/TU_NOMBRE/log_hito8_2.log`
- **Contenido:**  
  La salida del comando de Git que demuestra que:
  - el conflicto ha sido resuelto manualmente,
  - la fusión se ha completado correctamente,
  - y el repositorio vuelve a estar en un estado limpio.

### ✅ Criterios de evaluación

- El alumno modifica el mismo archivo y **la misma línea** en ambas ramas.
- El conflicto se produce al fusionar las ramas en local.
- El conflicto se resuelve manualmente, eligiendo una versión de forma consciente.
- La mezcla se completa correctamente.
- Las evidencias existen, tienen el nombre correcto y contienen salidas reales de Git.
