# Ready to upload

This project is cleaned for GitHub upload.

## Before running locally
Create a `.env.local` file:

```env
NEXT_PUBLIC_MAPBOX_TOKEN=your_public_mapbox_token_here
ZOHO_FLOW_WEBHOOK_URL=https://flow.zoho.sa/150001185639/flow/webhook/incoming?zapikey=1001.f45c7403ec1d68cc362baa9f53cd9b23.9a0a725956e52c0ea7abb3091f5d094e&isdebug=false
```

## Before deploying
Add these environment variables in your hosting provider:

- `NEXT_PUBLIC_MAPBOX_TOKEN`
- `ZOHO_FLOW_WEBHOOK_URL`

## What changed
- The check-in form now sends data to `/api/checkin`
- `/api/checkin` forwards the JSON payload to your Zoho Flow webhook
- Zoho Flow can then create a record in Zoho Creator

## Important
- Do not commit `.env.local`
- Use a public Mapbox token that starts with `pk.`
- Keep `ZOHO_FLOW_WEBHOOK_URL` server-side only and never expose it with `NEXT_PUBLIC_`
- If an old token was pushed before, rotate it in Mapbox
