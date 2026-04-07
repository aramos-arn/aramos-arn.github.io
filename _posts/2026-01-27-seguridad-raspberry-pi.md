---
layout: default
title: "Bastionado de Red Doméstica con Raspberry Pi"
date: 2026-01-27
categories: [Seguridad, SysAdmin, Linux]
excerpt: "Guía para la puesta en marcha de Pi-hole con Raspberry Pi"
---
# Bastionado de Red Doméstica con Raspberry Pi

En este proyecto documento cómo he configurado una defensa perimetral para mi red doméstica utilizando hardware de bajo coste. El objetivo es bloquear telemetría y dominios maliciosos a nivel de DNS.

### 🛠️ Arquitectura
* **Hardware:** Raspberry Pi 4
* **Software:** Pi-hole (DNS Sinkhole) + Unbound (Recursive DNS)
* **Acceso Remoto:** WireGuard VPN

### 🚀 Instalación y Configuración
El primer paso fue asegurar el sistema operativo (Raspberry Pi OS) creando un usuario con privilegios limitados y deshabilitando el acceso root por SSH.

```bash
# Ejemplo de actualización y bastionado inicial
sudo apt update && sudo apt upgrade -y
# Configuración de firewall UFW
sudo ufw allow 51820/udp  # Puerto WireGuard
sudo ufw enable
```
