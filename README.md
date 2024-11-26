# InformeFrontDocker

(Esto es solo un resumen basado en mis practicas)

**2. Fundamentos**

Docker es una herramienta de contenedorización que permite empaquetar aplicaciones y sus dependencias en contenedores portátiles y reproducibles. Al utilizar Docker en proyectos frontend, se asegura que la aplicación pueda ejecutarse de manera consistente en cualquier entorno, evitando problemas de compatibilidad entre sistemas operativos o versiones de dependencias.

En el caso de aplicaciones frontend, Docker puede ser usado para contenerizar entornos de desarrollo, servidores web como Nginx para servir archivos estáticos y para la integración con otros servicios en un entorno completo.

**3. Conocimientos previos**

.Conceptos básicos de Docker: imágenes, contenedores, volúmenes y redes.

.Frontend Development: Familiaridad con frameworks como React, Angular, Vue.js, etc.

.Configuración de servidores web: Uso de Nginx o Apache para servir aplicaciones frontend.

.Gestores de paquetes: npm o yarn para manejar dependencias.

.Docker Compose: Para orquestar el frontend con otros servicios como un backend o bases de datos.

.Control de versiones: Uso básico de Git.

**4. Objetivos a alcanzar**

.Contenerizar una aplicación frontend usando Docker.

.Facilitar la integración del frontend con otros servicios en un entorno contenedorizado.

.Simplificar el despliegue en entornos locales y en la nube.

.Implementar un flujo de trabajo eficiente para desarrollo, pruebas y producción.

**5. Equipo necesario**

.Docker y Docker Compose instalados.

.Un editor de texto o IDE como VS Code, WebStorm o similar.

.Sistema operativo compatible: Linux, macOS o Windows con WSL2.

.Proyecto frontend existente (React, Angular, Vue.js o aplicaciones web estáticas).

**6. Material de apoyo**

.Documentación oficial de Docker

.Tutoriales específicos para contenerización de aplicaciones frontend.

.Guías de configuración de Nginx para servir archivos estáticos.

**7. Procedimiento**

Tener instalado docker en nuestro equipo de trabajo, una vez instalado debemos crear una carpeta llamada nginx y dentro de esta una carpeta conf.d y creamos un archivo defaul.conf que debe tener lo siguiente: 

![image](https://github.com/user-attachments/assets/93eb9e68-3abb-4fe0-828c-47cd15763ae9)

esto ayudara a que conectemos el backend con el fronted y se pueda usar esos datos

Creamos un archivo nginx.conf que tendra lo siguiente: 

![image](https://github.com/user-attachments/assets/e1e38f93-3510-445a-84db-bc795b2eab4e)

Ahora hay que crear un archivo dockerfile dentro de la raiz del proyecto que tendra lo siguiente:

![image](https://github.com/user-attachments/assets/159046b2-dddc-45af-96e8-34f4daceeaff)

![image](https://github.com/user-attachments/assets/48d866e0-0606-49bf-8224-10f34e6f9424)

Esto nos ayudara en cuando comenzamos a descargar el proyecto usando docker hara que el dockerfile instale las dependecias necesarias para que el proyecto se cree de manera correcta.

Abrimos un terminal de linux y entramos al directorio donde esta ubicado el proyecto:

![image](https://github.com/user-attachments/assets/cb4b6f7a-67aa-4106-b852-faf9883423e3)

usando mnt ayudara a encontrar archivos que estan ubicados en la maquina de windows en mi caso seria en mi disco duro.

Creamos un nano docker-compose.yml que debe tener lo siguiente: 

![image](https://github.com/user-attachments/assets/ef756540-4594-4831-a742-651e8f89e410)

El codigo que esta escrito en la imagen ayudara a que se inicie el proyecto incluyendo que se descargue de manera correcta porque el proyecto esta ciendo creado con react, y se debe de guardar los cambios con ctrl+o para guardar y ctrl+x para salir.

Se debe aplicar lo siguientes comando para crear el proyecto: 

.docker-compose build 

.docker-compose up -d

El proyecto se creara correctamente y se puede visualizar.

![image](https://github.com/user-attachments/assets/145c9c24-7f14-42ef-9d41-e7006779efff)


**8. Resultados esperados**

.Una imagen Docker funcional que contiene el frontend con sus dependencias.

.Flujo de trabajo simplificado para desarrolladores que puedan usar el contenedor sin problemas de configuración.

.Capacidad de servir la aplicación desde un contenedor en cualquier entorno.

.Integración eficiente del frontend con otros servicios mediante Docker Compose.

**9. Bibliografía**

-Docker Inc. (n.d.). Docker Documentation. Retrieved from https://docs.docker.com/

-Nginx. (n.d.). Official Nginx Documentation. Retrieved from https://nginx.org/en/docs/
