# Filippo Beer Sommelier Website

Official repository for the Filippo Beer Sommelier website.

## Current release

- Release candidate: MVP v1.7
- Hosting: OVHcloud
- Newsletter provider: Brevo
- Public contact: `info@filippobeersommelier.it`
- Production status: pending live deployment and smoke test

## Deployment

Production deployment is performed manually from GitHub Actions using:

`.github/workflows/deploy-ovh.yml`

The approved ZIP must be stored at:

`release/filippo-beer-sommelier-site-MVP-v1.7-Deployment-Candidate.zip`

Required repository environment secrets:

- `OVH_FTP_SERVER`
- `OVH_FTP_USERNAME`
- `OVH_FTP_PASSWORD`
- `OVH_FTP_PORT`
- `OVH_FTP_REMOTE_DIR`

The workflow validates and extracts the release archive before mirroring the site to OVHcloud. Production is declared only after the live smoke test passes.
