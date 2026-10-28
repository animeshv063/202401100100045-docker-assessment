# CA-2 Practical Assessment: Docker & Container Security

### 1. Student & Service Information
- **Name:** Animesh Verma
- **Class:** CS - A
- **Registration Number:** 202401100100045
- **Assigned Port:** 8045 (calculated using rule: 80 + last 2 digits of REGNO -> 80 + 45 = 8045)
- **Docker Hub Username:** animeshv063
- **Docker Hub Link:** https://hub.docker.com/r/animeshv063/fest-backend

---

### 2. AI Tools Declaration
Used Gemini (Antigravity) to help debug Dockerfile build errors, format the Docker Compose file with network isolation, and look up the exact syntax for trivy and cosign flags.

---

### 3. Backend Image Digest (v1.0.0)
`sha256:7f4c391bb4d5e9a08905b63481ccbb3e66a3d129a08a47814b72cf7f79f9024c`

---

### 4. Vulnerability Remediation Table (Stage 3.3)

| Metric | fest-backend:0.1 (Base: python:3.9) | fest-backend:0.2 (Hardened: python:3.11-slim) |
| :--- | :--- | :--- |
| **CRITICAL Vulnerabilities** | 8 | 0 |
| **HIGH Vulnerabilities** | 34 | 0 |
| **Final Image Size** | ~920 MB | ~165 MB |

**Summary of fixes made:**
1. Switched the base image from `python:3.9` to `python:3.11-slim` to eliminate outdated OS packages.
2. Created a dedicated non-root user (`appuser` with UID 1000) inside the Dockerfile instead of running the app as root.
3. Updated dependencies in `requirements.txt` to current secure versions (Flask 3.0.3, Werkzeug 3.0.3, psycopg2-binary 2.9.10).
4. Verified that running `trivy image --severity CRITICAL --ignore-unfixed --exit-code 1 fest-backend:0.2` exits with code 0.

---

### 5. Incomplete Steps
None. All 5 stages were completed according to the assessment specifications.
