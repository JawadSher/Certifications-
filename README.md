# Certifications

A public archive of my professional certifications, credentials, and completed courses — shared for verification and reference alongside my [portfolio](https://jawadsher.github.io) and [GitHub profile](https://github.com/JawadSher).

## About

This repository is the single source of truth for every certification I've earned across web development, cybersecurity, and computer science. It's consumed live by the **Certifications** section on my portfolio site — push an image and a JSON entry here, and it shows up there. No redeploy, no manual sync.

Each entry is verifiable and linked directly from my portfolio site and professional profiles (LinkedIn, Upwork, Fiverr).

## How it works

`certifications.json` is the manifest. The portfolio site fetches it directly from this repo, so this file — not the folder layout — is what actually controls what appears, in what order, and with what detail.

Adding a certificate is two steps:

1. Drop the certificate file into the matching category folder (create a new one if needed).
2. Add one entry for it to `certifications-info` in `certifications.json`.

That's it — nothing in the portfolio codebase ever needs to change.

## Repository Structure

```
Certifications/
├── certifications.json     # manifest — powers the portfolio's Certifications section
├── web-development/
│   └── aws-cloud-practitioner-2026.png
├── cybersecurity/
│   └── ejpt-2026.png
├── academic/
│   └── vu-transcript-2026.pdf
└── README.md
```

Folders are just for keeping files organized by category — the category shown on the portfolio comes from the `category` field in `certifications.json`, not the folder name. A file's folder and its `category` value don't have to match, but keeping them aligned makes the repo easier to navigate.

## `certifications.json` schema

```json
{
  "certifications-info": [
    {
      "id": "aws-cloud-practitioner-2026",
      "title": "AWS Certified Cloud Practitioner",
      "issuer": "Amazon Web Services",
      "issueDate": "2026-03-01",
      "credentialId": "ABCD1234",
      "credentialUrl": "https://www.credly.com/badges/example",
      "image": "web-development/aws-cloud-practitioner-2026.png",
      "category": "Cloud",
      "featured": true,
      "description": "Covers core AWS services, pricing, and cloud fundamentals.",
      "skills": ["AWS", "Cloud Architecture", "Cost Management"]
    }
  ]
}
```

| Field           | Type              | Required | Notes                                              |
| --------------- | ----------------- | -------- | --------------------------------------------------- |
| `id`            | `string`          | Yes      | Unique per entry; used as the list key on the site   |
| `title`         | `string`          | Yes      | Certificate name                                     |
| `issuer`        | `string`          | Yes      | Issuing organization                                 |
| `issueDate`     | `string` (`YYYY-MM-DD`) | Yes | Drives newest → oldest sorting on the site          |
| `credentialId`  | `string \| null`  | No       | Shown in the credential detail if present            |
| `credentialUrl` | `string \| null`  | No       | Powers the "Verify Credential" link                  |
| `image`         | `string`          | Yes      | Path to the file, relative to the repo root          |
| `category`      | `string`          | Yes      | Powers the category filter on the site               |
| `featured`      | `boolean`         | No       | Adds a "Featured" badge on the site                  |
| `description`   | `string`          | No       | Short summary shown in the detail panel              |
| `skills`        | `string[]`        | No       | Rendered as tags in the detail panel                 |

## Verification

All certificates listed here are authentic and can be independently verified through the issuing organization's official verification portal, linked via each entry's `credentialUrl` where available.

## Usage & Rights

All certificates, documents, and images in this repository are the property of **Jawad Sher** and are shared publicly for verification and portfolio purposes only. Redistribution, reproduction, or reuse of these documents without explicit permission is not permitted.

## Connect

- **Portfolio:** [jawadsher.github.io](https://jawadsher.github.io)
- **GitHub:** [@JawadSher](https://github.com/JawadSher)
- **LinkedIn:** _add link_
