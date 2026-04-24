# IDOR Lab Writeup

## 🧪 Lab Name

User Account Access Control Bypass

---

## 🐞 Vulnerability Type

Insecure Direct Object Reference (IDOR)

---

## 📌 Description

The application uses predictable user IDs in requests without verifying ownership.

---

## 🔍 Steps to Reproduce

1. Log in as a normal user.
2. Open profile request in browser or Burp Suite.
3. Change:

/account?id=1001

to

/account?id=1002

4. Another user's data becomes visible.

---

## ⚠️ Impact

An attacker may access:

- Personal data
- Orders
- Invoices
- Sensitive records

---

## 🛡️ Recommended Fix

- Server-side authorization checks
- Validate object ownership
- Use indirect references

---

## 🎯 Platform

Practice Lab
