<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/0119dfcd-7433-4561-8da3-693ab3ab355c

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`

## PocketBase configuration

The application uses PocketBase for authentication and application data. Start
the local server with:

```powershell
C:\pocketbase.exe serve --dir=C:\projects\deroua-services\pocketbase_data --http=127.0.0.1:8090
```

Create `.env.local` from `.env.example` and set:

```env
VITE_POCKETBASE_URL="http://127.0.0.1:8090"
```

After creating a PocketBase superuser, initialise or update the database schema
with `npm run pocketbase:setup`. For production, use an HTTPS endpoint and set
the three `POCKETBASE_*` environment variables before running that command.
"# deroua-services-app" 
