# RansomwareSim – Laboratorio en Kali Linux DJ

## Descripción

Este proyecto implementa una simulación completa de ransomware utilizando **RansomwareSim** en **Kali Linux**.  
El flujo consiste en cifrar archivos ubicados en un directorio específico, enviar la clave de cifrado a un servidor de control y recuperar los archivos únicamente a través de dicho servidor.

---

## Cambios implementados

Esta versión ya incluye los siguientes cambios aplicados:

1. Compatibilidad con Linux (eliminación de `USERPROFILE`)
2. Creación del archivo `Readme.txt` en el directorio de ejecución
3. Uso obligatorio del directorio objetivo `dosyalar/`
4. Ejecución correcta de `Encoder.py`, `Decoder.py` y `ControlServer.py` en Kali Linux

No es necesario modificar manualmente el código.

---

## Requisitos

- Kali Linux (VirtualBox)
- Python 3
- Git
- Entorno virtual de Python (`venv`)

---
