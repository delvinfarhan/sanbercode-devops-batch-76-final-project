# Klinik Health - Final Project DevOps

Final Project DevOps Sanbercode Batch 76.

Project ini merupakan implementasi deployment website klinik ke environment production menggunakan metode **Artifact Build** pada VPS Ubuntu.

Website dideploy menggunakan **Nginx Reverse Proxy, PM2 Process Management, HTTPS (SSL), serta workflow CI/CD sederhana menggunakan GitHub Actions**.

> Credit template website: HTMLCodex

---

## Live Demo

🔗 https://klinik-health.duckdns.org

---

## Overview Project

Project ini menggunakan website klinik sebagai simulasi sistem layanan kesehatan di dunia nyata.

Website layanan kesehatan membutuhkan stabilitas, keamanan, dan availability yang baik karena ketika terjadi gangguan sistem dapat berdampak pada akses informasi penting terkait layanan medis.

Fokus utama project ini adalah membangun deployment environment yang stabil, aman, ringan dijalankan pada VPS 512MB, dan dapat diakses publik menggunakan HTTPS.

---

## Tech Stack

- **Operating System:** Ubuntu 24.04
- **Web Server:** Nginx
- **Process Manager:** PM2
- **Domain Provider:** DuckDNS
- **SSL:** Let's Encrypt / Certbot
- **Repository:** GitHub
- **Deployment Method:** Artifact Build
- **CI/CD:** GitHub Actions
- **Frontend:** HTML, CSS, JavaScript

---

## Arsitektur Deployment

```text
User Browser
      ↓ HTTPS
Nginx Reverse Proxy
      ↓
PM2 Service (Port 3000)
      ↓
Clinic Website
```

---

## Fitur yang Diimplementasikan

- Deployment VPS Ubuntu  
- SSH Access VPS  
- Nginx Reverse Proxy  
- PM2 Process Management  
- HTTPS / SSL  
- UFW Firewall  
- Resource Optimization (512MB VPS)  
- Basic CI/CD menggunakan GitHub Actions  

---

## Alur CI/CD

```text
Push Code ke GitHub (main branch)
            ↓
GitHub Actions Trigger
            ↓
SSH ke VPS
            ↓
Git Pull Repository Terbaru
            ↓
Restart PM2 & Nginx
            ↓
Website Otomatis Ter-update
```

---

## Alasan Menggunakan Artifact Build

Metode Artifact Build dipilih karena:

- Lebih sesuai dengan hands-on task selama bootcamp
- Lebih ringan untuk VPS 512MB
- Proses deployment dan maintenance lebih sederhana
- Lebih efisien resource dibanding container untuk project ini

Docker diperkenalkan pada pertemuan akhir sebagai materi tambahan, sedangkan deployment berbasis artifact lebih banyak digunakan selama proses pembelajaran.
