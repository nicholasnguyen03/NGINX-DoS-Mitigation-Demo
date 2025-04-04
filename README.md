# NGINX DoS Mitigation Demo

This project demonstrates how to configure and test basic DoS (Denial of Service) mitigation techniques on an NGINX server using timeout rules and request rate limiting. It includes configuration changes, attack simulation using Slowloris, and packet capture analysis.

---

## 🔧 Configuration Overview

- Modified `/etc/nginx/nginx.conf` to include:
  - `limit_req_zone` for IP-based rate limiting
- Updated `/etc/nginx/conf.d/default.conf` to include:
  - `limit_req` directive to apply the rate limit
  - Timeout rules: `client_header_timeout`, `client_body_timeout`, and `keepalive_timeout`

---

## 💥 Attack Simulation

- Simulated a Slowloris attack using:
  ```bash
  slowloris 127.0.0.1
