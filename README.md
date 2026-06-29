# FastWork Updates

Private update manifest for FastWork Monitor.

Use this repository as private storage for:

- `versions.json` - update manifest read by the app.
- release zip assets - one zip per app version.

Recommended GitHub setup:

1. Create a private repository named `Uniq-Low/fast-work-updates`.
2. Push this folder to the repository.
3. Upload each version zip as a GitHub Release asset with the same tag and filename used in `versions.json`.
4. Create a fine-grained GitHub token with read-only access to repository Contents.
5. Put that token into FastWork settings under `Токен доступа к версиям`.

The app's default manifest URL is:

```text
https://raw.githubusercontent.com/Uniq-Low/fast-work-updates/main/versions.json
```

Do not embed the token into the exe. Anyone with the exe can extract embedded secrets.
