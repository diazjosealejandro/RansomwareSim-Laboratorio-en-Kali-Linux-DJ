# RansomwareSim – Laboratorio en Kali Linux DJ

## Descripción

Este proyecto implementa una simulación completa de ransomware utilizando **RansomwareSim** en **Kali Linux**.  
El flujo consiste en cifrar archivos ubicados en un directorio específico, enviar la clave de cifrado a un servidor de control y recuperar los archivos únicamente a través de dicho servidor.

---

## Cambios realizados al proyecto original

Se realizaron los siguientes cambios para garantizar el correcto funcionamiento y coherencia del proyecto en Kali Linux:

### Encoder.py
- Se eliminó el uso de `USERPROFILE` y se reemplazó por `os.getcwd()` para compatibilidad con Linux.
- Se cambió el directorio objetivo de `dosyalar/` a `victima/`.
- Se configuró la IP correcta del servidor de control.
- Se agregó un banner visual al inicio de la ejecución.
- Se incorporó un registro de actividad (`activity.log`) para los archivos cifrados.
- Se añadió un contador final que muestra el total de archivos cifrados.
- Se añadió una pausa (`sleep`) para simular el tiempo de cifrado.
- Se mantuvo la extensión personalizada `.denizhalil` para los archivos cifrados.

### ControlServer.py
- Se mantuvo el puerto y comportamiento base del servidor.
- Se mejoró la salida en consola mostrando claramente:
  - Datos recibidos desde la víctima.
  - Clave de cifrado almacenada en el servidor.
  - Solicitudes de clave realizadas por el decoder.
- Se mejoró el registro en `server_log.txt` para distinguir entre recepción y entrega de claves.
- Se mantuvo soporte para múltiples conexiones mediante threading.

### Decoder.py
- Se eliminó el uso de `USERPROFILE` y se reemplazó por `os.getcwd()`.
- Se sincronizó el directorio objetivo con `victima/`.
- Se configuró la IP correcta del servidor de control.
- Se mantuvo el mecanismo de solicitud de clave al servidor.
- Se agregó la eliminación automática del archivo `Readme.txt` tras el descifrado.
- Se mantuvo limpieza de memoria al finalizar la ejecución.

### Estructura final del proyecto
- Se estableció el uso obligatorio del directorio `victima/`.
- Se unificaron IP, puerto y extensiones entre todos los módulos.
- Se garantizó la coherencia del flujo:
  Encoder → ControlServer → Decoder.

---

## Requisitos

- Kali Linux (VirtualBox)
- Python 3
- Git
- Entorno virtual de Python (`venv`)

---
