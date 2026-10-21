# Payments hotfix — SEC-1042

Incident: SEC-1042 — Proxy-Authorization header leaked to upstream hosts on redirect.

Scope of this hotfix:
- Introduce a pinned requirements.txt for the payments service.
- requests pinned at 2.31.0 (contains the Proxy-Authorization fix).
- urllib3 pinned at 2.2.1.
- flask stays at 2.0.1 (out of scope, do not touch).

Pre-merge check (required): confirm whether any GitHub global security advisories
affect the pinned versions of requests, urllib3, and flask, and record the
findings as review comments on the pull request.
