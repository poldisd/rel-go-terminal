# REL<GO> — Relationship Map Terminal

Bloomberg-Terminal-Style Beziehungsnetzwerk-Explorer (Holders, Board, Banks, Kunden, Lieferanten).

## Deploy auf Vercel
1. Repo zu deinem GitHub pushen / hochladen
2. Auf vercel.com → "Add New" → "Project" → dieses Repo auswählen → Deploy
3. **Wichtig für die Firmen-Suche:** In Vercel → Project → Settings → Environment Variables:
   - Name: `ANTHROPIC_API_KEY`
   - Wert: dein API-Key von console.anthropic.com (Get API Keys)
   - Danach: Deployments → neuestes Deployment → "Redeploy" (damit die Env-Var greift)

Ohne diesen Key funktioniert die Karte für die 4 Demo-Firmen (LNG, BKR, AAPL, TSLA) trotzdem —
nur die freie Suche nach anderen Firmen braucht den Key, da sie über `/api/generate.js`
serverseitig Claude aufruft (Kosten fallen dabei über deinen Anthropic-Account an).

## Lokal öffnen
`index.html` direkt im Browser öffnen (Suche funktioniert dann nicht, da `/api/generate` ein Server braucht).
