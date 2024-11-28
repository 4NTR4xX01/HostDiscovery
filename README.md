# HostDiscovery.sh

Este es un script básico que te permitiría poder encontrar hosts activos dentro de una red
Puede ser usado el cualquier tipo de reto CTF, para temas de Pivoting, etc.


#!/bin/bash

for i in $(seq 1 254); do
        timeout 1 bash -c "ping -c 10.10.0.$i" &>/dev/null && echo "[+] Host 10.10.0.$i - ACTIVO" &

done; wait


