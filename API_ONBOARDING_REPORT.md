# API Onboarding Report – Dog CEO API

## 1. Resumen de la API

- **Nombre de la API:** Dog CEO API (Dog Pics)
- **Base URL:** https://dog.ceo/api
- **Tipo de autenticación:** No requiere autenticación
- **Rate limit:** No especificado en la documentación oficial

La Dog CEO API es una API pública que permite obtener imágenes de perros organizadas por razas y sub-razas. Está diseñada para consumo sencillo, no requiere autenticación y responde en formato JSON, lo que la hace adecuada para pruebas, prototipos y aprendizaje del consumo de APIs REST.

---

## 2. Tabla de Endpoints

| Método | URL | Query Params | Headers | Status esperado | Status obtenido |
|------|-----|--------------|---------|-----------------|-----------------|
| GET | /breeds/list/all | N/A | Accept: application/json | 200 | 200 |
| GET | /breed/{breed}/images/random | N/A | Accept: application/json | 200 | 200 |
| GET | /breed/{breed}/images | N/A | Accept: application/json | 200 | 200 |
| GET | /breed/{breed}/list | N/A | Accept: application/json | 200 | 200 |
| GET | /breed/{breed}/{subbreed}/images/random | N/A | Accept: application/json | 200 | 200 |
| GET | /breeds/image/random/{n} | n | Accept: application/json | 200 | 200 |
| GET | /breed/noexiste/images | N/A | Accept: application/json | 404 | 404 |
| GET | /breed//images | N/A | Accept: application/json | 400 | 404 |
| GET | /status/401 (endpoint de prueba) | N/A | Accept: application/json | 401 | 401 |
| GET | /status/403 (endpoint de prueba) | N/A | Accept: application/json | 403 | 403 |

**Nota:**  
La API Dog CEO no diferencia explícitamente entre errores 400 y 404 para URLs malformadas, por lo que algunos requests con error esperado 400 retornan 404.

---

## 3. Evidencia de respuestas

### Solicitudes exitosas
Se validaron múltiples solicitudes con respuesta **200 OK**, incluyendo:
- Listado completo de razas.
- Obtención de una imagen aleatoria por raza.
- Obtención de múltiples imágenes aleatorias.
- Consulta de sub-razas y filtrado por sub-raza específica.

### Solicitudes fallidas
- **404 Not Found:** al consultar una raza inexistente.
- **Request malformado:** URL inválida que retorna error.
- **401 y 403:** la API Dog CEO no requiere autenticación, por lo que estos códigos no aplican de forma nativa. Para evidenciar dichos códigos HTTP se utilizaron endpoints de prueba externos.

---

## 4. Observaciones finales

La Dog CEO API es una API simple y consistente, adecuada para prácticas de consumo de APIs REST. Su falta de autenticación simplifica las pruebas, aunque limita la demostración de errores de autorización, los cuales fueron suplidos mediante endpoints de prueba para cumplir con los requerimientos del laboratorio.