# Keylogger Script

Este repositorio contiene un conjunto de scripts para capturar entradas de teclado en sistemas Linux y Windows. 
El propósito de estos scripts es demostrar cómo se puede implementar un keylogger básico en diferentes entornos.

# GitBook de `Keylogger Script`:

URL = [Pincha aquí](https://dise0.gitbook.io/h4cker_b00k/tecnica-keylogger-automatizada/keylogger-script-automatizado-linux-y-windows)

## Contenido

- **capture_victim.py** y **server_host.py**: Scripts principales en Python para capturar entradas de teclado. Compatible con entornos gráficos y de terminal.
- **requirements.sh**: Script para instalar las dependencias necesarias para ejecutar el script Python.

## Instalación de Requisitos

### 1. `requirements.sh`

El script `requirements.sh` se encarga de instalar las bibliotecas necesarias para ejecutar el script `Python`. Asegúrate de ejecutar este script con privilegios de `root`.

**Instrucciones para ejecutar `requirements.sh`:**

### 2. **Descargar o clonar el repositorio**:

   ```bash
   git clone https://github.com/D1se0/keylogger_script.git
   cd keylogger_script
   ```

## Hacer el script ejecutable:

 ```bash
 chmod +x requirements.sh
 ```

## Ejecutar el script como root:

 ```bash
 sudo ./requirements.sh
 ```

Este script instalará `pynput`, `keyboard`, y `colorama`, que son necesarios para el funcionamiento del script `Python`.

## Uso del Script

### 3. `server_host.py`

Este script recive las capturas de teclado por el script `capture_victim.py`. 
Disponible para entorno grafico y terminal.

### 4. `capture_victim.py`

Este script captura las entradas de teclado y las envía a un servidor especificado. Dependiendo del entorno, puede utilizar diferentes bibliotecas para capturar las entradas:

Entorno Gráfico: Utiliza `pynput`.
Entorno de Terminal: Utiliza `keyboard`.

## Para ejecutar el script:

Asegúrate de que todas las dependencias estén instaladas (ver Instalación de Requisitos).

## Configura el script:

Edita `capture_victim.py` y `server_host.py` para definir la dirección IP y el puerto del servidor al que se enviarán las entradas y capturas de teclado.

## Ejecuta el script en la maquina atacante:

```bash
python3 server_host.py
```

## Ejecuta el script en la maquina victima:

```bash
python3 capture_victim.py
```

## Reverse Shell

Tambien a parte de proporcionar las capturas de teclado se crea una reverse shell con el sistema de la maquina victima mediante un `msfvenom` que tendremos que configurar acorde a los ajustes de los scripts.
Tendremos que cargar en metasploit el modulo de `multi/handler` y configurarlo para estar a la escucha.

## Nota de Seguridad

Este script se proporciona con fines educativos. Usar un `keylogger` sin el permiso explícito del usuario es ilegal y éticamente incorrecto. 
Asegúrate de tener siempre la autorización adecuada antes de ejecutar o distribuir software de captura de teclas.

## Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar el script o agregar nuevas características, siéntete libre de hacer un `pull request`.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

## Contacto

Para cualquier pregunta o comentario, por favor contacta a `ciberseguridad12345@gmail.com`.

¡Gracias por utilizar el repositorio `Keylogger Script`!
