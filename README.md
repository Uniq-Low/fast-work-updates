# FastWork Updates

Private update manifest for FastWork Monitor.

Use this repository as private storage for:

- `versions.json` - update manifest read by the app.
- release zip assets - one zip per app version.

Recommended GitHub setup:

1. Create a private repository named `Uniq-Low/fast-work-updates`.
2. Push this folder to the repository.
3. Put `versions.json` into the repository root.
4. Host each version zip at the exact `downloadUrl` from `versions.json`.
5. If the manifest or zip endpoint is private, create a read-only token and put it into FastWork settings under `Токен доступа к версиям`.

Important: the app downloads the zip itself from `downloadUrl`. Use a direct HTTPS endpoint that returns the file to the app. A private GitHub Release browser URL may redirect in a way that does not preserve the token; a public/unguessable release asset URL or a private file server/object storage URL is more reliable for zip files.

The app's default manifest URL is:

```text
https://raw.githubusercontent.com/Uniq-Low/fast-work-updates/main/versions.json
```

Do not embed the token into the exe. Anyone with the exe can extract embedded secrets.
