# FestPass Containerisation & Security Assessment (CA-2)

## 1. Student & Service Information
- **Name:** Animesh Verma
- **Registration Number (REGNO):** 202401100100045
- **Assigned Port (PORT):** 8045 (Calculated as 80 + last two digits: `80` + `45` = `8045`)
- **Docker Hub Username:** animeshv063
- **Docker Hub Repository:** https://hub.docker.com/r/animeshv063/fest-backend
- **GitHub Repository:** https://github.com/animeshv063/202401100100045-docker-assessment

---

## 2. AI Tools Declared
- **Tools Used:** Antigravity (Gemini)
- **Usage:** Assisted in structuring the multi-stage Dockerfiles, Docker Compose service isolation and health checks, analyzing Trivy vulnerability reports, and formatting Cosign signing commands.

---

## 3. Image Digest (fest-backend:1.0.0)
- **Digest:** `sha256:7f4c391bb4d5e9a08905b63481ccbb3e66a3d129a08a47814b72cf7f79f9024c`

---

## 4. Trivy Vulnerability Scan Comparison (Stage 3.3)

| Metric | Before (`fest-backend:0.1` - python:3.9) | After (`fest-backend:0.2` - python:3.11-slim non-root) |
| :--- | :--- | :--- |
| **CRITICAL Vulnerabilities** | 8 | 0 |
| **HIGH Vulnerabilities** | 34 | 0 |
| **Image Size** | 920 MB | 165 MB |

---

## 5. Incomplete Steps
- *None. All stages (1 through 5) completed successfully.*
