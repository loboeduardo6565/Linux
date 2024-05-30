# Linux

# Linux Cheat Sheet

## Monitoreo de CPU

1. **`top`**
   - Muestra los procesos en ejecución y el uso de recursos en tiempo real.

2. **`htop`**
   - Una versión mejorada de `top` con una interfaz más amigable.

3. **`mpstat`**
   - Muestra estadísticas de CPU.

4. **`sar -u 1 3`**
   - Muestra el uso de CPU cada segundo durante tres segundos.

5. **`vmstat 1 5`**
   - Muestra estadísticas de sistema, incluyendo CPU, memoria y I/O.

6. **`iostat -c`**
   - Muestra estadísticas de CPU.

7. **`uptime`**
   - Muestra el tiempo de actividad del sistema y la carga promedio.

8. **`nproc`**
   - Muestra el número de CPUs disponibles.

9. **`lscpu`**
   - Muestra información detallada sobre la arquitectura de la CPU.

10. **`ps -eo pcpu,pid,user,args | sort -k 1 -r | head -10`**
    - Muestra los 10 procesos que más CPU consumen.

## Monitoreo de Memoria

11. **`free -h`**
    - Muestra el uso de memoria en formato legible para humanos.

12. **`vmstat -s`**
    - Muestra estadísticas de memoria.

13. **`top`**
    - Incluye información sobre el uso de memoria.

14. **`htop`**
    - Incluye información sobre el uso de memoria.

15. **`cat /proc/meminfo`**
    - Muestra información detallada de la memoria.

16. **`watch -n 1 free -h`**
    - Muestra el uso de memoria y se actualiza cada segundo.

17. **`ps -eo pmem,pid,user,args | sort -k 1 -r | head -10`**
    - Muestra los 10 procesos que más memoria consumen.

18. **`smem`**
    - Muestra el uso de memoria por proceso.

19. **`sar -r 1 3`**
    - Muestra el uso de memoria cada segundo durante tres segundos.

20. **`dmidecode --type 17`**
    - Muestra información sobre los módulos de memoria RAM.

## Monitoreo de Disco

21. **`df -h`**
    - Muestra el uso del sistema de archivos en formato legible para humanos.

22. **`du -sh [directorio]`**
    - Muestra el tamaño de un directorio específico.

23. **`lsblk`**
    - Lista la información de los dispositivos de bloque.

24. **`iostat -dx`**
    - Muestra estadísticas de I/O de disco para todos los dispositivos.

25. **`iotop`**
    - Muestra el uso de I/O por proceso en tiempo real.

26. **`dstat`**
    - Muestra estadísticas del sistema, incluyendo disco.

27. **`smartctl -a /dev/sda`**
    - Muestra el estado SMART de un disco.

28. **`blkid`**
    - Muestra identificadores de dispositivo de bloques.

29. **`hdparm -I /dev/sda`**
    - Muestra información detallada de un disco.

30. **`df -i`**
    - Muestra el uso de inodos.

## Monitoreo de Red

31. **`ifconfig`**
    - Muestra la configuración de interfaces de red.

32. **`ip a`**
    - Muestra información detallada de las interfaces de red.

33. **`netstat -tuln`**
    - Muestra todas las conexiones de red y puertos en escucha.

34. **`ss -tuln`**
    - Similar a `netstat`, pero más moderno y rápido.

35. **`ping [host]`**
    - Comprueba la conectividad con un host.

36. **`traceroute [host]`**
    - Muestra la ruta que toman los paquetes para llegar a un host.

37. **`mtr [host]`**
    - Combina `ping` y `traceroute` para mostrar la ruta y la latencia en tiempo real.

38. **`iftop`**
    - Muestra el uso de ancho de banda por conexión en tiempo real.

39. **`nload`**
    - Muestra el uso de ancho de banda en tiempo real.

40. **`ip -s link`**
    - Muestra estadísticas de enlace de red.

## Monitoreo de Errores y Logs

41. **`dmesg`**
    - Muestra mensajes del anillo de buffer del kernel.

42. **`dmesg | grep -i error`**
    - Filtra los errores en los mensajes del kernel.

43. **`journalctl`**
    - Muestra logs del sistema gestionados por `systemd`.

44. **`journalctl -xe`**
    - Muestra logs del sistema con detalles adicionales y seguimiento en vivo.

45. **`journalctl -u [servicio]`**
    - Muestra logs para un servicio específico gestionado por `systemd`.

46. **`tail -f /var/log/syslog`**
    - Muestra los últimos registros del archivo de logs del sistema y sigue nuevos registros.

47. **`tail -f /var/log/messages`**
    - Similar a `syslog`, pero para sistemas que utilizan `messages`.

48. **`grep -i error /var/log/syslog`**
    - Filtra los errores en el archivo de logs del sistema.

49. **`ausearch -m avc`**
    - Busca eventos de control de acceso en los logs de `auditd` (usado en SELinux).

50. **`logwatch --detail high`**
    - Genera un informe detallado de los logs del sistema.

##### Enlaces de interes:

https://www.linuxjournal.com/content/how-secure-your-website-openssl-and-ssl-certificates
