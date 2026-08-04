# SLP Releases

This repository contains the official Android APK releases and update metadata for the E.M.P.O.W.E.R. application.

## Latest Release Metadata

The application checks this file for available updates:

```text
latest.json
```

Raw URL:

```text
https://raw.githubusercontent.com/alduanemirasol/SLP-releases/main/latest.json
```

## Release Files

Each GitHub release may include:

```text
empower-arm64-v8a-v<version>.apk
empower-armeabi-v7a-v<version>.apk
empower-x86_64-v<version>.apk
empower-universal-v<version>.apk
```

### APK Types

* `arm64-v8a` – Most modern Android devices
* `armeabi-v7a` – Older 32-bit Android devices
* `x86_64` – Android emulators and x86 devices
* `universal` – Fallback APK for supported devices

## Update Metadata Format

```json
{
  "version": "1.0.10",
  "tag": "v1.0.10",
  "notes": [
    "Added new features",
    "Fixed application issues"
  ],
  "assets": [
    {
      "name": "empower-arm64-v8a-v1.0.10.apk",
      "downloadUrl": "https://github.com/alduanemirasol/SLP-releases/releases/download/v1.0.10/empower-arm64-v8a-v1.0.10.apk",
      "sizeBytes": 31485605
    }
  ]
}
```

## Publishing a New Release

1. Build the APK files.
2. Create a Git tag using the format:

```text
v<version>
```

Example:

```text
v1.0.11
```

3. Create a GitHub release using the same tag.
4. Upload the APK files.
5. Update `latest.json`.
6. Verify that the version, tag, filenames, and download URLs match.
7. Commit and push the updated metadata.

## Version Format

Use semantic versioning:

```text
MAJOR.MINOR.PATCH
```

Example:

```text
1.0.10
```

## Important Rules

* Keep `latest.json` valid.
* Use direct GitHub Release download URLs.
* Do not use GitHub `/blob/` URLs in the application.
* Do not delete APK files from active releases.
* Keep release notes short and based on actual changes.
* Test all APK download links before publishing.
