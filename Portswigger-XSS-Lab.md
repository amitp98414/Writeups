# PortSwigger XSS Lab Writeup

## 🧪 Lab Name
Reflected XSS into HTML Context with No Encoding

---

## 🐞 Vulnerability Type
Reflected Cross-Site Scripting (XSS)

---

## 📌 Description
The application reflects user-controlled input inside the HTML response without proper sanitization or output encoding.

---

## 💥 Payload Used

<script>alert(1)</script>

---

## 🔍 Steps to Reproduce

1. Open the vulnerable search page.
2. Enter the payload into the search box.
3. Submit the request.
4. JavaScript alert executes successfully.

---

## ⚠️ Impact

An attacker can execute arbitrary JavaScript in the victim's browser, leading to:

- Session hijacking
- Credential theft
- Phishing attacks
- DOM manipulation

---

## 🛡️ Recommended Fix

- Apply output encoding
- Sanitize user input
- Use Content Security Policy (CSP)

---

## 🎯 Platform

PortSwigger Web Security Academy
