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
- La jornada 1 es Bricomaniacos FC 2–1 Piso Piloto (según la clasificación oficial de MLA).
- La jornada 11 no se ha inventado: no venía en el calendario facilitado.
- Colores de la web tomados del escudo: rosa #e484a8, negro #0f0d0e y crema #fbf4f1.
- Menú: Inicio · Plantilla, Crónicas · Calendario, Clasificación · MVP, Porra, Pronósticos (sin Economía ni Colaboradores).

## Panel privado
Entra por `/login.html`. El acceso se valida en el servidor mediante `ADMIN_PASSWORD`.

## Clasificación de MLA Sport (grupo 4708)
- La clasificación oficial ya viene cargada (jornada 1) en `data/data.json`.
- Se actualiza sola **los domingos cada hora, de 16:00 a 22:00 (hora de Madrid)**, leyendo https://www.mlasport.com/clasificacion-grupo/4708 (variable opcional `MLA_URLS`, varias URLs separadas por comas).
- Si MLA falla, se conservan los últimos datos (2 reintentos cada 10 min dentro de la misma hora).
- Cuando hay resultados nuevos se recalculan las cuotas automáticas del próximo partido.
- Prueba manual a cualquier hora: `POST /api/mla/sync` (admin).
