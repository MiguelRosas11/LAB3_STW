# Lab 3 – Dog CEO API (Sistemas y Tecnologías Web)

## Descripción

Este laboratorio consiste en la exploración y consumo de una API REST pública utilizando Postman y HTTPie.  
La API seleccionada fue **Dog CEO API**, la cual permite obtener imágenes de perros organizadas por razas y sub-razas.



## API Seleccionada

- **Nombre:** Dog CEO API  
- **Base URL:** https://dog.ceo/api  
- **Autenticación:** No requiere autenticación  
- **Tipo:** REST API  



## Contenido del Repositorio

Este repositorio incluye:

- `API_ONBOARDING_REPORT.md`  
  Documento con el análisis de la API, tabla de endpoints y evidencia de respuestas.

- `httpie-commands.md`  
  Archivo con los comandos equivalentes en HTTPie para las solicitudes realizadas en Postman.

- `dog-api-environment.json`  
  Environment exportado de Postman con variables reutilizables.

- `lab3_dog_api.postman_collection.json`  
  Colección de Postman que incluye:
  - Happy Path (casos exitosos)
  - Errores intencionales (404, 400, 401, 403)



## Estructura del Trabajo en Postman

### Happy Path
Incluye solicitudes exitosas (200 OK) que cubren:
- Listado de razas
- Obtención de imagen por raza
- Obtención de múltiples imágenes
- Consulta de sub-razas
- Filtro por sub-raza

### Errores Intencionales
Incluye:
- 404 Not Found
- Request malformado
- 401 Unauthorized (endpoint de prueba)
- 403 Forbidden (endpoint de prueba)


## Notas

La API Dog CEO no requiere autenticación, por lo que los códigos 401 y 403 no aplican de forma nativa.  
Para cumplir con los requerimientos del laboratorio, se utilizaron endpoints de prueba para evidenciar dichos códigos HTTP.



## Autor

Miguel Rosas  
Universidad del Valle de Guatemala  
Sistemas y Tecnologías Web – Semestre 1, 2026
