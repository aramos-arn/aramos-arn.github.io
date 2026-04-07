---
layout: default
title: "Bastionado de servicio VNC ante ataques de Fuerza Bruta con Fail2ban"
date: 2026-04-07
categories: [Seguridad, SysAdmin, Linux]
excerpt: "Guía práctica para securizar un servicio TightVNC expuesto a internet, automatizando el bloqueo de atacantes mediante Fail2ban e iptables."
---
# Bastionado de servicio VNC ante intentos de acceso y fuerza bruta

En este post documentamos cómo configurar fail2ban para proteger un servicio VNC expuesto a internet.
El objetivo es monitorizar los logs del servicio y bloquear dinámicamente a nivel de firewall (iptables) las direcciones IP que superen un umbral de intentos fallidos.

## 🛠️ 1. Configuración de la "Jail" (Prisión)
En primer lugar crearemos una nueva seccion en el fichero /etc/fail2ban/jail.local de la siguiente manera:
```ini
[tightvnc]
enabled = true       # podemos habilitar o deshabilitar el filtro
port    = 5901       # el puerto a proteger
filter  = tightvnc   # el nombre que damos al servicio
logpath = /home/user/.vnc/host:1.log    # Ruta al log
maxretry = 3        # Número máximo de intentos antes de ser baneado
findtime = 600      # Tiempo en el que permiten los fallos indicados en maxretry (segundos)
bantime  = 86400    # Tiempo de baneo (segundos)
```
continuaremos...
