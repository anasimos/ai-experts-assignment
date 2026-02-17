# AI Experts Assignment (Python) — Solution 🚀

This repository contains a robust implementation of the HTTP Client, featuring critical fixes for state mutation and authentication logic errors.

---

## 🛠 How to Run Locally
Get the project running on your machine in three simple steps:

**1. Create and activate a virtual environment:**
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

**2. Install pinned dependencies:**
```bash
pip install -r requirements.txt
```

**3. Execute the test suite:**
```bash
pytest -v
```

---

## 🐳 How to Run with Docker
This project is fully containerized to ensure consistent results across any environment.

**1. Build the image:**
```bash
docker build -t ai-experts-assignment .
```

**2. Run the containerized tests:**
```bash
docker run ai-experts-assignment
```

---

## 🔍 Bug Identification & Resolution
The following engineering issues were identified and corrected to ensure the client is production-ready:

* **Header Mutation:** Fixed a bug where the `request` method was modifying the input `headers` dictionary in-place, causing unintended side effects for the caller.
* **Refresh Logic:** Corrected the logic gate that failed to trigger a token refresh when the `oauth2_token` was in a raw dictionary or `None` state.
* **Regression Testing:** Added comprehensive tests in `tests/test_http_client.py` to reproduce the identified bugs and verify the fixes.

---

## 📁 Project Structure
* **app/** — Core application logic including the HTTP Client and Token models.
* **tests/** — Pytest suite containing original and new regression tests.
* **Dockerfile** — Configured for non-interactive, CI-style test execution.
* **requirements.txt** — Project dependencies with strictly pinned versions.
* **EXPLANATION.md** — Detailed technical breakdown of the bugs and the reasoning behind the fixes.

---

**Author:** Anasimos Tesfaye
**Status:** ✅ 7/7 Tests Passing