Para configurar un proyecto colaborativo usando Git y GitHub desde cero, con Visual Studio Code (VS Code), sigue estos pasos. Involucra desde la creación del repositorio hasta la colaboración efectiva con un equipo:

### 1. **Instalación y configuración de Git**
   - Si no tienes Git instalado, instálalo desde [git-scm.com](https://git-scm.com/).
   - Configura Git con tu nombre y correo para todos los commits que hagas:
     ```bash
     git config --global user.name "TuNombre"
     git config --global user.email "tuemail@ejemplo.com"
     ```

### 2. **Creación del proyecto en GitHub**
   - Ve a [GitHub](https://github.com) y crea una cuenta si no la tienes.
   - Crea un **nuevo repositorio** desde la interfaz de GitHub. Elige un nombre (por ejemplo, `club-deportivo-web`).
   - Marca la opción **"Initialize this repository with a README"** para tener un archivo base.
   - Añade un archivo **.gitignore** y selecciona "Node" o cualquier otro según el stack que uses, para evitar subir archivos innecesarios.

### 3. **Agregar colaboradores en GitHub**
   - En la página de tu repositorio, ve a `Settings > Collaborators`.
   - Añade a los miembros de tu equipo mediante sus nombres de usuario de GitHub, para que todos puedan colaborar en el repositorio.

### 4. **Clonar el repositorio en tu máquina**
   - Copia el enlace HTTPS del repositorio desde GitHub.
   - Abre **Visual Studio Code** y abre la terminal integrada (`Ctrl + ñ` o desde `View > Terminal`).
   - Ejecuta el siguiente comando para clonar el repositorio en tu máquina local:
     ```bash
     git clone https://github.com/tuusuario/club-deportivo-web.git
     ```
   - Cambia al directorio del proyecto:
     ```bash
     cd club-deportivo-web
     ```

### 5. **Inicializa tu proyecto web**
   - Crea los archivos necesarios para la página web del club deportivo en tu carpeta local:
     ```bash
     /club-deportivo-web
     ├── index.html
     ├── styles.css
     └── script.js
     ```
   - Realiza los cambios iniciales, como el diseño de la página, y guarda los archivos.

### 6. **Realiza el primer commit**
   - Una vez que hayas terminado los primeros cambios, agrega los archivos al área de preparación:
     ```bash
     git add .
     ```
   - Realiza tu primer commit:
     ```bash
     git commit -m "Estructura básica del sitio web del club deportivo"
     ```

### 7. **Sube el código al repositorio remoto**
   - Para enviar tu trabajo a GitHub:
     ```bash
     git push origin master
     ```

### 8. **Flujo colaborativo para el equipo**
   
   #### 8.1. **Crear ramas (branches) para nuevas características**
   - Cada desarrollador debe crear una nueva rama para trabajar en una funcionalidad sin afectar el código principal:
     ```bash
     git checkout -b nombre-rama
     ```
   - Por ejemplo, si estás trabajando en la página de inicio, podrías usar:
     ```bash
     git checkout -b pagina-inicio
     ```

   #### 8.2. **Subir cambios en la rama**
   - Después de hacer cambios en la rama, súbelos a GitHub:
     ```bash
     git add .
     git commit -m "Descripción de los cambios"
     git push origin nombre-rama
     ```

   #### 8.3. **Realizar un Pull Request (PR)**
   - Una vez que termines tu trabajo, ve a GitHub y crea un **Pull Request (PR)** desde tu rama hacia la rama `master` o `main`.
   - Los demás colaboradores pueden revisar los cambios y sugerir modificaciones antes de hacer el merge.
   - Después de la revisión, alguien con permisos de escritura puede aprobar y hacer el **merge** del PR.

   #### 8.4. **Mantener el código actualizado**
   - Para asegurarse de que todos trabajen con la última versión del código, el equipo debe ejecutar `git pull` regularmente en la rama principal:
     ```bash
     git checkout master
     git pull origin master
     ```

   #### 8.5. **Resolver conflictos de merge**
   - Si varios desarrolladores trabajan en las mismas partes del código, pueden ocurrir conflictos al hacer merge. Git indicará los archivos en conflicto, y tendrás que resolverlos manualmente. Una vez resueltos, sigue con:
     ```bash
     git add archivo-en-conflicto
     git commit -m "Conflictos resueltos"
     git push origin nombre-rama
     ```

### 9. **Colaboración a través de Issues y Proyectos**
   - **Issues**: Usa la sección de Issues en GitHub para registrar tareas, errores o nuevas características. Cualquiera puede asignarse tareas o discutir los problemas.
   - **Proyectos**: Puedes crear un tablero tipo Kanban en la sección de `Projects` para organizar las tareas del equipo, asignando issues y PRs a diferentes columnas.

### 10. **Extensiones útiles para la colaboración en VS Code**
   - **GitLens**: Facilita ver el historial de los archivos, autores de cambios y revisar la trazabilidad de commits.
   - **GitHub Pull Requests**: Gestiona los PR directamente desde VS Code.
   - **Live Share**: Permite a los desarrolladores colaborar en tiempo real en el código desde sus VS Code.

### Resumen del flujo de trabajo colaborativo:
1. **Cada miembro clona el repositorio**.
2. **Cada tarea o funcionalidad se desarrolla en una rama separada**.
3. **Los cambios se suben a GitHub mediante commits y pushes**.
4. **Se realizan Pull Requests para revisión de código**.
5. **Se hace merge de la rama a la principal tras la aprobación**.
6. **Todos actualizan el código con `git pull` regularmente**.

Este flujo permite que todo el equipo trabaje en paralelo sin generar conflictos en el código principal.
