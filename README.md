# 🔍 Reverse Engineering — Allsafe (Vulnerable APK)

[![Platform](https://img.shields.io/badge/Platform-Android-green)](https://play.google.com) [![Focus](https://img.shields.io/badge/Focus-Reverse%20Engineering-orange)]() [![Status](https://img.shields.io/badge/Status-Lab%20Report-blue)]()

**Allsafe** is a purposely vulnerable Android application built for learning — not for break-ins. It simulates realistic mobile app flaws using modern libraries and patterns, making it an ideal target for reverse engineering and mobile security testing.

> _This repo contains my practical reverse-engineering walkthroughs and solved challenges for the Allsafe APK. Work shown here is for educational purposes only._  
> GitHub / Walkthroughs: https://lnkd.in/eSEPsm-D

---

## 🚩 Quick Snapshot — Challenges I Solved
- **Insecure Logging** — Sensitive data leaked to logs  
- **Hardcoded Credentials** — Secrets embedded in app code/resources  
- **Cloud DB Misconfigurations** — Exposed backend/config endpoints  
- **SQL Injection** — Unsanitized inputs leading to data access  
- **Weak Client-Side Auth / PIN Bypass** — Logic flaws allowing unauthorized access

---

## 🧰 Tools & Techniques
Tools used across the analysis and exploit development:
- **jadx-gui** — static analysis & decompiled source review  
- **adb** — device interaction, APK installation, file pulls  
- **Frida** — dynamic instrumentation and runtime manipulation  

Common techniques: code decompilation, string/resource hunting, runtime hooking, API inspection, and crafted payloads.

---

## 🧭 How I Approached the App (brief)
1. **Recon (static)** — decompile APK with `jadx-gui`, search for suspicious strings, API keys, or insecure log statements.  
2. **Static triage** — locate authentication flow, DB access code, and input handling.  
3. **Dynamic testing** — run the app on device/emulator, use `adb logcat` to capture logs, and apply **Frida** hooks to bypass PIN checks and inspect runtime behavior.  
4. **Exploit & verify** — demonstrate PoC for hardcoded creds, SQLi, or misconfigurations and capture screenshots / logs as evidence.  
5. **Mitigation** — propose fixes like removing secrets, using parameterized queries, proper logging policies, and secure auth flows.

---

## ✅ What You’ll Find in This Repo
- Step-by-step **walkthroughs** for each solved challenge  
- Frida scripts & small helper tools used during testing  
- Notes on mitigation and secure redesign suggestions  
- Screenshots and PoC snippets (where applicable)

---

## 📘 Learning Outcomes
- How to locate and responsibly exploit common mobile issues (without causing harm)  
- Practical use of Frida for authentication bypass & runtime inspection  
- How insecure logging and hardcoded values translate to real risk  
- Defensive improvements: secure storage, input validation, and least-privilege practices

---

## ⚠️ Disclaimer
All content here documents analysis of a purposely vulnerable application for **educational purposes only**. Do **not** use these techniques against systems you do not have explicit permission to test. Respect laws and responsible disclosure practices.

---

## 📬 Connect / More
If you’re also into cybersecurity, feel free to connect:  
- 💻 LinkdenIn: [@muhammad-ahsanijaz](https://www.linkedin.com/in/muhammad-ahsanijaz/)   
- GitHub: `https://github.com/your-username` (replace with your profile)  
----
Don't forget to **follow** for more content 
⭐ If you find this repo helpful, consider giving this repo a **star** to support my work!  
