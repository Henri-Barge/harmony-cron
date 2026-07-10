# harmony-cron

Taktgeber für die Übungs-Erinnerungen von **Henri Harmony Guitar**
(https://henri-harmony-guitar.vercel.app).

- `tick.yml` ruft alle 10 Minuten `POST /api/tick` auf (Bearer `CRON_SECRET`).
  Der Endpoint prüft je Gerät und Zeitzone, welche der drei Übungszeiten fällig
  ist, und verschickt Web-Push-Nachrichten — auch bei geschlossener App.
- `keepalive.yml` pusht monatlich einen leeren Commit, damit GitHub die
  Scheduled-Workflows nicht nach 60 Tagen Inaktivität deaktiviert.

Gleiches Muster wie `agenda-cron`.
