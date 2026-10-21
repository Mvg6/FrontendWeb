# Evaluación de daños en fachadas — Frontend

Interfaz web de una aplicación que clasifica daños en fachadas de edificaciones después de
desastres naturales. Permite subir fotografías de una edificación, ver el análisis (tipo de
construcción, nivel de daño, si es rescatable y la recomendación), consultar el historial de
inspecciones y descargar reportes.

Es una sola página (`index.html`) sin dependencias de compilación. Las fuentes (Barlow y
Barlow Condensed) están en `fonts/`, bajo la licencia SIL Open Font License (`fonts/OFL.txt`).

Backend: https://github.com/Mvg6/BackendWeb

## Uso normal

El backend sirve este frontend en `http://localhost:8000/`, en el mismo origen que la API.
Para eso, clona los dos repositorios uno al lado del otro; la carpeta de este debe llamarse
`frontend`:

```bash
git clone https://github.com/Mvg6/BackendWeb.git backend
git clone https://github.com/Mvg6/FrontendWeb.git frontend
```

Luego sigue las instrucciones del README del backend para instalarlo y arrancarlo, y abre
`http://localhost:8000/` en el navegador.

## Abrirlo aparte (desarrollo)

También se puede abrir `index.html` con otro servidor local (por ejemplo, la extensión
Live Server de VS Code, en otro puerto) o directamente como archivo. En ese caso la página
detecta que no está en el puerto 8000 y se conecta al backend en `http://localhost:8000`.

Requisitos:

- El backend debe estar corriendo en `http://localhost:8000`.
- En el `.env` del backend, `MODO_PUBLICO=off` (con `on`, CORS solo acepta el mismo origen y
  el frontend abierto aparte no puede conectarse).
