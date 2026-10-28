# FestPass: Docker & Container Security Assessment (CA-2)

| Item | Value |
|---|---|
| Name | Prathmesh |
| REGNO | 202401100200235 |
| PORT | 8035 |
| Docker Hub username | innominate00 |
| Docker Hub repository | https://hub.docker.com/r/innominate00/fest-backend |

## AI tools used

- Claude Code (Anthropic): wrote the Dockerfile, `compose.yaml` and starter-file setup, explained errors, and guided me through the stages. I ran every command and took every screenshot myself on my own machine.

## Digest of 1.0.0 as pushed to Docker Hub

```
sha256:005618da975cbac8ea225803d4afe25fa8adabbc9bfe8885f8515264a197c6be
```

`innominate00/fest-backend:1.0.0` and `innominate00/fest-backend:1.0` point to this same digest.

## Vulnerability scan: before and after (Trivy)

| | `fest-backend:0.1` (python:3.9) | `fest-backend:0.2` (python:3.13-slim) |
|---|---|---|
| CRITICAL | 234 | 0 |
| HIGH | 2249 | 49 |
| Image size (disk usage) | 1.61GB | 248MB |

The gate command `trivy image --severity CRITICAL --ignore-unfixed --exit-code 1 fest-backend:0.2` exits with code 0.

## Steps I could not complete

None so far.
