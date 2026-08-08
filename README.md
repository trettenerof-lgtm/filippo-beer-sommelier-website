# Filippo Beer Sommelier Website

Official repository for the Filippo Beer Sommelier website.

## Current release

- Release candidate: Website v1.8 — Constitution Mode
- Canonical production URL: <https://filippobeersommelier.com/>
- Hosting: OVHcloud
- Newsletter provider: Brevo
- Public contact: `info@filippobeersommelier.it`

## Website v1.8 scope

- Independent `Viaggi` navigation branch
- Social Publishing Engine public landing page
- Public Privacy Policy and Terms of Service for TikTok Content Posting API
- TikTok site-verification files at the root and under `/social-publishing-engine/`
- Updated SEO, GEO and AI discovery files
- Canonical `.com` URLs throughout the release

## Deployment

Production deployment is performed by GitHub Actions using:

`.github/workflows/deploy-ovh.yml`

The approved archive and checksum are stored at the repository root:

- `filippo-beer-sommelier-site-v1.8-Deployment-Candidate.zip`
- `filippo-beer-sommelier-site-v1.8-Deployment-Candidate.zip.sha256`

The workflow verifies the checksum, validates the v1.8 package, and mirrors the static website to OVHcloud through SFTP. It uses the `production` environment secret `OVH_FTP_PASSWORD`.

Production is declared synchronized only after the GitHub Actions run succeeds and the live smoke test passes.
