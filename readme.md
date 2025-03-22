# Propuesta de desarrollo

## Introducción

Se requiere un sitio web que incluya una landing page, un panel de administración para dicha landing page, un blog, un formulario para registro de voluntarios, un mapa con marcadores y una pasarela de pago en la cual se acepten pagos mensuales o pagos únicos, cuyo monto sea definido por el usuario.

## Especificaciones

### Landing page

Es necesario coordinar con el cliente las secciones de la landing page y cuáles de estas secciones van a ser editables desde el panel de administación.
Es necesario crear un usuario con rol administrador (valorar si será el único usuario o si habrán otros).

Estructura propuesta de la Landing Page:
- Navegación fija: Un menú de navegación el la parte superior del sitio, se muestran algunos enlaces relevantes que facilitan la navegación por el sitio web.
- Cabecera: Una sección en la que se mostratán imágenes y/o algún mensaje que represente el propósito de la organización y/o el sitio web. Es lo primero que suele ver el usuario al entrar al sitio web. 
- Sección "Sobre Nosotros": En esta sección se describiría la identidad de la organización, dejando claros los principios y valores de esta, así como la visión y misión de esta, de manera que el usuario pueda identificar lo que el sitio web le puede aportar.
- Sección "Objetivos" o "Servicios": Sección que complementa a la anterior, en caso de la anterior no ser suficiente. Esta sección es opcional
- Sección "Logros": Sección que valida los resultados de la organización, en esta se muestran premios obtenidos por la organización, y el número de objetivos alcanzados de una manera visual y, en algunos casos animada.
- Sección "Testimonios": Sección que muestra testimonios tanto de miembros de la organización como de personas que se hayan involucrado con esta.
- Sección "Donaciones": Aquí se agrega el enlace a la página de donaciones del sitio web.
- Sección "Blog": Sección en la que se agregan algunas publicaciones relevantes del blog y en enlace al mismo, para facilitar el acceso al blog al usuario y despertar el interés de este hacia el mismo.
- Sección "Contacto": Esta sección incluye un formulario destinado a que los usuarios interesados en el servicio brindado envíen alguna solicitud, testimonio o propuesta a los administradores del sitio web. 
- Pie de página (o Footer): En esta sección se muestran algunos enlaces relevantes en el sitio web (algunos que no necesariamente deben de aparecer en la navegación), información de contacto y redes sociales. Esta sección suele ser más abarcadora que la sección de navegación.

Algunas de las secciones de la landing page pueden ser modificables por el administrador, es necesario definir esas secciones.

### Blog

#### Vista "Lista de blogs"
Debe de crearse una página que muestre las entradas de blog paginadas, cada entrada de blog dentro de esta vista puede mostrar:
- El título de la entrada
- Una imagen
- Fecha de publicación
- Una categoría
- Fecha de publicación
- Cantidad de vistas
- Número de comentarios
- Tiempo estimado de lectura

#### Vista "Publicación de blog"
Dentro de la vista de cada entrada de blog se debe de mostrar la información del blog completa (con el blog ya creado), al final de la sección los usuarios pueden hacer comentarios.
Dentro de esta vista puede haber una barra lateral que muestre otras entradas de blog relacionadas o destacadas.
Es importante definir cuales usuarios pueden enviar comentarios (definir si es necesario que sea un usuario autenticado y en caso de que así sea definir el rol de dicho usuario). 

#### Vista "Creación de blog"
Dentro de esta vista un usuario con rol de administrador podrá crear y modificar blogs de la plataforma, en esta vista se mostrará una entrada estilo formulario que permitirá al usuario elaborar el blog con todos los requisitos que desee.
En esta vista es necesario definir cuál será la estructura del blog que se creará.

Propuesta de campos de creación de blog:
Palabras clave: Listado de palabras clave de la publicación, útiles en el momento de colocar el sitio web en Google
Descripción: Es útil para colocar la publicación en Google, además de que se puede mostrar en la vista "Lista de blogs"
Imágenes: El listado de imágenes que se mostrarán en la publicación
Título: El título de la publicación
Cuerpo: El cuerpo de la publicación
Cabecera: En este campo opcional se pueden agregar imágenes interactivas
Publicaciones recomendadas: En este campo se puede elegir algunos blogs que se quieran recomendar en la barra lateral de la vsta "Publicación de blog" 

### Formulario de registro de voluntarios
Para este formulario debe de existir una vista, es necesario definir los datos requeridos en este formulario.

### Mapa con marcadores
Para este mapa debe de existir una vista, es necesario definir los datos requeridos en esta vista además del mapa.
Dentro del mapa habrán marcadores que definirá el administrador. El mapa incluirá funcionalidad para permitir a los administradores del sitio web agregar marcadores.

### Página de donaciones

En esta vista se agregarán dos enlaces, uno para hacer un pago único, y otro para crear una subscripción de pago mensual. De esta manera el usuario puede elegir la frecuencia con la que hace sus pagos. 

Es necesario definir la estrategia de pago y de desubscripción de los pagos.

### Autenticación y autorización de usuarios

Es necesario definir los roles necesarios para el sitio web y la estrategia de creación de usuarios.

Estrategias propuestas:
- Mantener un solo tipo de usuario con rol de administrador, que sea el que cree y modifique todo el contenido de la web, los usuarios sin autenticarse pueden hacer comentarios en el blog
- Definir tres tipos de usuarios: Adiministrador, Periodista y Consumidor
El administrador tendría potestad para modificar el sitio web desde el panel de administración y potestad para crear, eliminar y modificar blogs, además de crear usuarios tipo Periodista y Administrador
El periodista podría publicar y modificar publicaciones de blogs
El consumidor podría hacer comentarios dentro de los blogs.

## Equipo de trabajo disponible

Contamos con un equipo de 3 personas, dos programadores y un diseñador. Cada uno de estos con disponibilidad de 20 horas de trabajo a la semana.

Se propone el personal necesario y cualificado para agilizar el desarrollo de la plataforma sin comprometer su calidad.

## Tecnologías propuestas

### Tecnologias del lado del cliente
Estas son las tecnologías que se utilizan para el desarrollo del contenido a mostrar en el navegador de los usuarios, se utilizan marcos de trabajo basados en HTML, CSS y Javascript entre los que se incluyen los siguientes:

- ReactJs (https://es.react.dev/): Es un marco de trabajo basado en Javascript que extiende el HTML y facilita la creación y reutilización de componentes
- Tailwind (https://tailwindcss.com/): Es un marco de trabajo basado en CSS que facilita la creación de estilizados globales en un sitio web. Es una alternativa a Bootstrap y será usado para asegurar que el sitio web se mantenga responsive (adaptable a diferentes tamaños de pantalla) y permite la transición sencilla entre un tema claro y uno oscuro.
- React Leaflet (https://react-leaflet.js.org/): Es una adaptación de la librería Leaflet (https://leafletjs.com/) para el trabajo con mapas. Permite trabajar con mapas con licencias abiertas extraidos de https://www.openstreetmap.org/

Todas las librerías mencionadas son librerías con licencias libres, por tanto pueden ser usadas en proyectos privativos.

### Tecnologías del lado del servidor
Estas son las tecnologías que se utilizan para desarrollar en el servidor, en este lado de servidor debe de implementarse la capa de seguridad de la aplicación, entre estas se incluyen:

- NodeJs (https://nodejs.org/en): Es un lenguaje de programación del lado del servidor muy popular y flexible, tiene un ecosistema que permite enfocarse en la seguridad y velocidda del sitio web. 
- Stripe (https://stripe.com/es-us): Esta es la pasarela de pago a usarse, por razones de seguridad la lógica de su implementación debe de permanecer en el servidor.
- MySQL (https://www.mysql.com/): Es un motor de bases de datos ligero y con licencia abierta que puede integrarse dentro del servidor. Es necesario para persistir la información importante.
- nginx (https://nginx.org/): Es una aplicación de lado de servidor que se encarga de hacer de proxy de las peticiones del usuario (proxy inverso), con esta aplicación se añade una capa extra de seguridad a la aplicación
- Let's Encrypt (https://letsencrypt.org/): Es un servicio gratuito que permite que todo el tráfico de la aplicación viaje encriptado desde el cliente hasta el servidor, de manera que la información que sea interceptada no pueda ser descifrada. Esto añade una capa más de seguridad a la aplicación.

Todas las librerías mencionadas son librerías con licencias libres, por tanto pueden ser usadas en proyectos privativos.

### Despliegue

Para el despliegue la propuesta es el proveedor de servicios en la nube Digital Ocean (https://www.digitalocean.com/), este contiene un plan de pagos bastante adaptable a las necesidades particulares de cada proyecto (https://www.digitalocean.com/pricing/droplets), el equipo cuenta con experiencia utilizando este proveedor de servicios cloud y recomendamos su uso para el proyecto.

Para obtener el nombre de dominio proponemos Namecheap (https://www.namecheap.com/)

## Planificación de desarrollo

Proponemos realizar la aplicación en un tiempo estimado de 15 semanas contemplando una reunión semanal para medir avance, validar el trabajo realizado y plantear futuros cambios y funcionalidades. Proponemos el siguiente plan de acción:

- Diseño e implementación de la landing page: 3 semanas
- Diseño e implementación de la sección correspondiente al blog: 3 semanas
- Diseño e implementación de la sección de mapas: 1 semana
- Diseño e implementación de la sección de donaciones: 2 semanas
- Diseño e implementación de la sección de registro de voluntarios: 1 semana
- Diseño e implementación de secciones no contempladas: 2 semanas
- Pruenas orientadas a la seguridad del sitio web: 1 semana
- Despliegue del sitio web a un entorno de produccion: 2 semanas

Luego de desplegado el sitio web brindamos soporte a cualquier falla del sitio con respecto a los requisitos requeridos durante 8 semanas. Los requisitos extras serán valorados y agregados al presupuesto.

Luego de estas 8 semanas de mantenimiento gratuito se pueden elegir si nuestro equipo continúa brindándole soporte al sitio web o si requieren el código fuente para que otro equipo de desarrolladores desempeñe esta labor.

## Presupuesto

### Costes de producción del sitio

Los costes mencionados a continuación se describen en dólares americanos.

Costo total de mano de obra: 1800$
Costo estimado de despliegue:  18$ mensuales
Costo estimado del dominio: 10$ anuales

Costo de servicio de mantenimiento (20 dólares mensuales)

En caso de requerir un servidor de pruebas durante el desarrollo se cobrará el costo estimado del despliegue de manera mensual.

Los costos de agregar funcionalidades extras serán valorados con un presupuesto independiente.

El costo de mano de obra es hasta cierto punto negociable.

Los costos de despliegue pueden variar con el aumento o disminución del número de usuarios de la plataforma. Mientras ofrezcamos mantenimiento al sitio web nos encargaremos de optimizar el costo de despliegue sin afectar el rendimiento del sitio web.





