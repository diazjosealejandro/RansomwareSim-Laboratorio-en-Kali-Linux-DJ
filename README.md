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

## Instalación

# ACTUALIZAR SISTEMA E INSTALAR DEPENDENCIAS
sudo apt update
sudo apt install -y python3 python3-pip python3-venv git

# CLONAR REPOSITORIO
git clone https://github.com/TU_USUARIO/RansomwareSim-Linux.git
cd RansomwareSim-Linux

# CREAR Y ACTIVAR ENTORNO VIRTUAL
python3 -m venv venv
source venv/bin/activate

# INSTALAR DEPENDENCIAS DEL PROYECTO
pip install -r requirements.txt

# CREAR DIRECTORIO OBJETIVO
mkdir dosyalar

# CREAR ARCHIVOS DE PRUEBA
echo "Datos financieros" > dosyalar/finanzas.txt
echo "Listado de clientes" > dosyalar/clientes.txt
echo "Documento legal" > dosyalar/contrato.txt

# VERIFICAR CONTENIDO
ls dosyalar
