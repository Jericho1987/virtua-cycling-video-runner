# virtua-cycling-video-runner

Esegue su GitHub Actions il generatore dei video d'arrivo di Virtua Cycling.
Il motore e gli asset stanno in un repository privato; qui c'e' solo il workflow.

- Avvio a mano: Actions → "Video arrivo" → Run workflow → id della tappa.
- Avvio automatico: evento `repository_dispatch` di tipo `genera_video` con `client_payload: {"tappa": 157}`.

Secrets richiesti: `SUPABASE_URL`, `SUPABASE_SERVICE_KEY`, `VIDEO_REPO_TOKEN` (token di sola lettura sul repository del motore).
