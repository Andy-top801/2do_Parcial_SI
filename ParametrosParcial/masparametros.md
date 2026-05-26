Basado en las imágenes de la pizarra, tienes un proyecto universitario bastante completo para la materia de Sistemas de Información o similar. Se trata del desarrollo de una Aplicación Web para la admisión de alumnos nuevos a la FICCT, gestionando los procesos del CUP (Curso Universitario de Preparación) y el PSA (Prueba de Suficiencia Académica).

Aquí tienes el desglose exacto de lo que hay que hacer, las reglas del negocio, los plazos y una propuesta de arquitectura para que arranques.

🗓️ Cronograma y Entregables Clave
Presentación 1 (Ciclo #1): Domingo 31 de mayo hasta las 23:59 (Obligatoria).

Presentación 2 (Ciclo #2): Martes 09 de junio hasta las 23:59.

Defensa Final: Jueves 11 de junio a las 09:15.

Entregables Técnicos: URL del proyecto subido a la nube, Código QR que apunte a la app, repositorio en Git (Frontend, Backend, BD separada o estructurada).

💻 Stack Tecnológico Requerido
La pizarra es específica con las herramientas que debes usar:

Lenguaje / Backend: PHP.

Base de Datos: PostgreSQL.

Frontend: Debe ser una web Responsive (adaptable a móviles).

Infraestructura: Servidor en la nube (puedes usar servicios como Render, Railway, AWS o un hosting compartido básico).

Tip de desarrollo: Ya que el stack es PHP puro o framework, puedes apoyarte en agentes de IA que manejen el contexto completo de tu código (como Cursor, Cline o Copilot) para generar rápidamente el CRUD básico y la conexión PDO a PostgreSQL, ahorrándote tiempo para enfocarte en la lógica de los exámenes.

⚙️ Lógica y Reglas del Negocio (Lo que debe hacer la app)
El sistema debe gestionar Postulantes (alrededor de 1000 aspirantes) y distribuirlos cumpliendo estas reglas:

Gestión de Aulas y Grupos:

Capacidad máxima por aula: 60 alumnos.

Horarios disponibles: Mañana (M), Tarde (T), Noche (N).

El cupo total de admisiones es de 250 a 300 alumnos.

Gestión Académica (CUP):

Intervienen docentes de materias específicas: Computación (91), Matemáticas (95), Física (98) e Inglés.

Se toman 3 exámenes con las siguientes ponderaciones: 30%, 30% y 40%.

La nota mínima para aprobar es ≥ 60 puntos.

Reportes Requeridos:

Cantidad de alumnos aprobados.

Cantidad de alumnos reprobados.

El grupo con mayor cantidad de alumnos aprobados.

📄 Documentación Requerida (Metodología PUDS - UML)
El profesor exige una estructura documental formal. Debes armar un documento que contenga:

Perfil del Proyecto y Marco Teórico.

Ficha Técnica (F.T.): Aparece el acrónimo C-R-A-D-I-P (generalmente se refiere a las fases: Captura de requisitos, Análisis, Diseño, Implementación, Pruebas).

Diagramas UML (Obligatorios):

Diagrama de Casos de Uso (D.C.U.).

Diagrama de Comunicación.

Diagrama de Secuencia.

Bibliografía, Conclusión y Recomendación.

🚀 ¿Qué necesitas para empezar? (Plan de Acción)
Para que no empieces desde cero, aquí tienes la estructura base que deberías implementar:

1. Diseño de la Base de Datos (PostgreSQL):
Necesitarás al menos estas tablas principales:

postulante: ID, nombre, apellidos, CI, tipo_ingreso (CUP/PSA), estado (aprobado/reprobado).

materia: ID, nombre, codigo (91, 95, 98).

docente: ID, nombre, especialidad.

aula: ID, numero, capacidad (60).

grupo: ID, aula_id, docente_id, materia_id, horario (M/T/N).

postulante_grupo: Tabla intermedia para asignar alumnos a los grupos.

examen: ID, grupo_id, ponderacion (30, 30, 40).

calificacion: ID, postulante_id, examen_id, nota.

2. Tareas para tu equipo de trabajo:
Si estás trabajando en grupo, dividan el trabajo de inmediato:

Persona 1 (Documentación): Que empiece a redactar el Perfil, Marco Teórico y empiece a dibujar los Casos de Uso en herramientas como Draw.io o Lucidchart.

Persona 2 (Base de Datos & Backend): Que levante la base de datos en PostgreSQL, haga la conexión en PHP y prepare los endpoints o controladores para registrar postulantes.

Persona 3 (Frontend): Que diseñe las vistas HTML/CSS/JS (o usando Bootstrap/Tailwind para asegurar que sea responsive) de los formularios de registro y el panel de visualización de los reportes.

3. Enfoque inmediato para el 31 de Mayo:
Como la "Presentación 1" está muy cerca, asegúrate de tener listo al menos el Registro de Postulantes, la Asignación de Grupos/Aulas, el esquema de la base de datos y el Diagrama de Casos de Uso. Deja los reportes complejos para el Ciclo 2.