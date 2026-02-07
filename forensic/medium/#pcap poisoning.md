# [Challenge Name] - Writeup

## 📋 Info
**Category:** Web Exploitation  
**Points:** 150  
**Difficulty:** Medium  

**Description:**
> Can you exploit this website to get the flag?
> http://mercury.picoctf.net:PORT/

---

## 🎯 Solution Summary
**Attack:** SQL Injection with WAF bypass  
**Method:** Used `||` instead of `OR` to bypass filter  
**Flag:** `picoCTF{sql_byp4ss_w0rk5}`

---

## 🔍 Step-by-Step

### 1. Reconnaissance
Opened website, found login form. Tested basic SQLi:
````sql
' OR 1=1--   → Blocked!
````

### 2. Bypass Discovery
Tried alternative operators:
````sql
' || 1=1#    → Success!
````

### 3. Exploitation
**Burp Repeater:**
- Intercepted login POST
- Changed password to: `' || 1=1#`
- Forwarded request

**Result:** Logged in as admin, flag displayed

### 4. Flag Extraction
