# Keylogger Script

This repository contains a set of scripts for capturing keyboard input on Linux and Windows systems. 
The purpose of these scripts is to demonstrate how a basic keylogger can be implemented in different environments.

# GitBook of `Keylogger Script`:

URL = [Click here](https://dise0.gitbook.io/h4cker_b00k/tecnica-keylogger-automatizada/keylogger-script-automatizado-linux-y-windows)

## Content

- **capture_victim.py** and **server_host.py**: Core Python scripts for capturing keyboard input. Compatible with graphical and terminal environments.
- **requirements.sh**: Script to install the necessary dependencies to run the Python script.

## Installation Requirements

### 1. `requirements.sh`

The `requirements.sh` script is responsible for installing the necessary libraries to run the `Python` script. Make sure you run this script with `root` privileges.

**Instructions to run `requirements.sh`:**

### 2. **Download or clone the repository**:

   ```bash
   git clone https://github.com/D1se0/keylogger_script.git
   cd keylogger_script
   ```

## Make the script executable:

 ```bash
 chmod +x requirements.sh
 ```

## Run the script as root:

 ```bash
 sudo ./requirements.sh
 ```

This script will install `pynput`, `keyboard`, and `colorama`, which are necessary for the `Python` script to function.

## Use of the Script

### 3. `server_host.py`

This script receives the keycaps by the `capture_victim.py` script. 
Available for graphical and terminal environment.

### 4. `capture_victim.py`

This script captures keyboard input and sends it to a specified server. Depending on the environment, you can use different libraries to capture the inputs:

Graphical Environment: Use `pynput`.
Terminal Environment: Use `keyboard`.

## To run the script:

Make sure all dependencies are installed (see Installation Requirements).

## Configure the script:

Edit `capture_victim.py` and `server_host.py` to define the IP address and port of the server to which keystrokes and inputs will be sent.

## Run the script on the attacking machine:

```bash
python3 server_host.py
```

## Run the script on the victim machine:

```bash
python3 capture_victim.py
```

##ReverseShell

Also, apart from providing the keyboard captures, a reverse shell is created with the system of the victim machine using a `msfvenom` that we will have to configure according to the settings of the scripts.
We will have to load the `multi/handler` module into metasploit and configure it to listen.

## Security Note

This script is provided for educational purposes. Using a keylogger without the user's explicit permission is illegal and ethically wrong. 
Make sure you always have proper authorization before running or distributing keylogging software.

## Contributions

Contributions are welcome. If you want to improve the script or add new features, feel free to make a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contacto

Para cualquier pregunta o comentario, por favor contacta a `ciberseguridad12345@gmail.com`.

¡Gracias por utilizar el repositorio `Keylogger Script`!
