
# 🔍 Actividad 4: Escaneo de Seguridad con OWASP ZAP

## 🧠 Tema
Identificación de vulnerabilidades con **OWASP ZAP**.

## 🎯 Objetivo
Usar **OWASP ZAP** para encontrar y corregir vulnerabilidades en una aplicación web.

## 🛠️ ¿Qué es OWASP ZAP?

**ZAP (Zed Attack Proxy)** es una herramienta de escaneo de seguridad dinámica (DAST) que detecta vulnerabilidades como:

- Cross-Site Scripting (XSS)
- Inyección SQL (SQLi)
- Configuraciones inseguras

🔗 Sitio oficial: [https://www.zaproxy.org/](https://www.zaproxy.org/)

---

## 📦 Instalación de OWASP ZAP

```bash
sudo apt install zaproxy
```

### ✅ Verificar la instalación

```bash
zaproxy -daemon -port 8080 -host 127.0.0.1
```

---

## 🚀 Ejecutar un escaneo contra una aplicación web

### Aplicación objetivo: OWASP Juice Shop

Pasos para lanzar el escaneo:

1. Abrir **OWASP ZAP**.
2. Ingresar la URL de la aplicación vulnerable:  
   `http://localhost:3000`
3. Seleccionar **"Escaneo Automático"** y ejecutar el análisis.

---

## 🛡️ Ejemplos de vulnerabilidades detectadas

- Reflected XSS:  
  `/search?q=<script>alert('XSS')</script>`

- Posible inyección SQL:  
  `/login`

---

## 🧰 Mitigación y Mejores Prácticas

- Revisar el informe generado por ZAP y corregir las vulnerabilidades.
- Automatizar escaneos en pipelines de **CI/CD** para prevenir fallos antes del despliegue.

---

> 📘 Esta actividad forma parte del módulo de análisis de seguridad en aplicaciones web.
