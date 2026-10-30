# Bricomaniacos FC

Web de fútbol 7 basada en el proyecto aportado, con identidad visual y escudo conservados, pero navegación reorganizada y datos iniciales vacíos.

## Arranque
- Node.js 18 o superior
- `npm install`
- `ADMIN_PASSWORD=una-clave-larga npm start`

Configura `ADMIN_PASSWORD` como variable de entorno obligatoria para habilitar el panel privado. No uses una contraseña por defecto.

## Datos
- La plantilla, jugadores, votos, historial, porra y usuarios comienzan vacíos.
- El calendario de la temporada está cargado en `data/data.json`.
- La jornada 1 se muestra como Bricomaniacos FC 1–2 Piso Piloto, porque el dato recibido era Piso Piloto 2–1 Bricomaniacos FC.
- La jornada 11 no se ha inventado: no venía en el calendario facilitado.
- El escudo y los colores originales del ZIP se conservan.

## Panel privado
Entra por `/login.html`. El acceso se valida en el servidor mediante `ADMIN_PASSWORD`.
