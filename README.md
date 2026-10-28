# FestPass: Docker & Container Security (CA-2)

- **Name:** Kanishka Lodhi
- **REGNO:** 202401100200163
- **PORT:** 8063
- **Docker Hub username:** kanishkaa780
- **Docker Hub repository:** https://hub.docker.com/r/kanishkaa780/fest-backend

## AI tools used
- Claude: step-by-step guidance, drafting the Dockerfiles and compose.yaml, and explaining errors. I ran every command myself on my own machine.

## 1.0.0 digest (as pushed to Docker Hub)
`sha256:5cd2f447d1562da49343059a2c31760c8f1c51ebcf1b4edc151bf00282c892fe`

## Vulnerability scan: before and after

| | `fest-backend:0.1` | `fest-backend:0.2` |
|---|---|---|
| Base image | python:3.9 | python:3.13-slim-bookworm |
| CRITICAL | 234 | 2 (none with a fix) |
| HIGH | 2249 | 64 |
| Image size (disk / content) | 1.61GB / 412MB | 223MB / 54.3MB |

`trivy image --severity CRITICAL --ignore-unfixed --exit-code 1 fest-backend:0.2` exits with code 0.

## Incomplete steps
- Stage 5 (cosign sign and verify): not completed yet.