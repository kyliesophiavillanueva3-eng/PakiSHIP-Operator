# PakiSHIP Operator

React Native mobile app for PakiSHIP hub operators. Built with Expo + TypeScript.

## Setup

```bash
npm install
Copy-Item .env.example .env   # Windows PowerShell
# cp .env.example .env        # macOS/Linux
```

Set values in `.env`:
- `RN_PUBLIC_APP_NAME`
- `RN_PUBLIC_APP_ENV` (development | staging | production)
- `RN_PUBLIC_API_BASE_URL`

## Run

```bash
npm start
npm run android
```

## CI/CD

Set repository variable `MOBILE_SINGLE_SYSTEMS_JSON`:
```json
{ "name": "PakiSHIP-Operator", "dir": ".", "mobile_stack": "react-native" }
```

Pipeline triggers on push/PR to `test`, `uat`, `main`.

## Notes

- `android/` is committed. `ios/` must be generated on macOS via `npx expo prebuild --platform ios`.
- All source files are `.ts`/`.tsx` — no `.js`/`.jsx` in app source dirs.
- Run `npm run verify` before creating a PR.
