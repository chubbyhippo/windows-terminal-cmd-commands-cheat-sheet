# Windows Terminal Cheat Sheet

### **General Commands**
| Command                   | Description                                                                          |
|---------------------------|--------------------------------------------------------------------------------------|
| `cls`                    | Clears the terminal screen.                                                          |
| `exit`                   | Closes the terminal session.                                                         |
| `echo <text>`            | Displays <text> in the terminal.                                                     |
| `help`                   | Lists available commands.                                                            |

---

### **Task and Process Management**
| Command                               | Description                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------|
| `tasklist`                            | Displays all currently running processes.                                   |
| `taskkill /PID <process_id>`          | Kills a process using its Process ID (PID).                                 |
| `taskkill /IM <process_name>`         | Kills a process using its Image Name (e.g., `taskkill /IM notepad.exe`).    |
| `tskill <process_name_or_id>`         | Terminates a process by ID or name (e.g., built-in lightweight alternative).|

---

### **File Operations**
| Command                                            | Description                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| `dir`                                             | Lists all files and directories in the current directory.             |
| `cd <dir_path>`                                    | Changes the working directory to `<dir_path>`.                        |
| `mkdir <dir_name>`                                 | Creates a new directory named `<dir_name>`.                           |
| `del <file_name>`                                  | Deletes a specific file.                                              |
| `del /f /q <file_name>`                            | Deletes a file forcefully and quietly (without confirmation).         |
| `del /s /q <dir_name>`                             | Deletes all files inside a directory recursively.                     |
| `rmdir /s /q <dir_name>`                           | Removes a folder and its contents recursively.                        |

---

### **Networking**
| Command                                | Description                                                              |
|----------------------------------------|--------------------------------------------------------------------------|
| `ipconfig`                             | Displays network configuration details.                                  |
| `ipconfig /all`                        | Displays all details (including MAC address, DNS info, etc.).            |
| `ipconfig /release`                    | Releases the current IP address.                                        |
| `ipconfig /renew`                      | Renews and requests a new IP address lease from the DHCP server.         |
| `ping <hostname_or_ip>`                | Tests connectivity with a specific host or IP address.                   |

---

### **System Operations**
| Command                        | Description                                                                 |
|--------------------------------|-----------------------------------------------------------------------------|
| `shutdown /s /t 0`             | Shuts down the system immediately.                                         |
| `shutdown /r /t 0`             | Restarts the system immediately.                                           |
| `shutdown /l`                  | Logs off the current user.                                                 |
| `systeminfo`                   | Displays detailed system information.                                      |

---

### **Disk and File System Operations**
| Command                                 | Description                                                             |
|-----------------------------------------|-------------------------------------------------------------------------|
| `chkdsk <drive_letter>: /f /r`          | Checks and repairs filesystem errors and bad sectors on a drive.        |
| `format <drive_letter>: /fs:<file_system>` | Formats a drive with the specified filesystem (`NTFS`, `FAT32`, etc.).  |

---

### **Power Commands**
| Command                        | Description                                                                 |
|--------------------------------|-----------------------------------------------------------------------------|
| `powercfg /list`               | Displays a list of all available power schemes.                            |
| `powercfg /hibernate on`       | Enables hibernation mode.                                                  |
| `powercfg /hibernate off`      | Disables hibernation mode.                                                 |

---

### **Environment and Variables**
| Command                    | Description                                                                    |
|----------------------------|--------------------------------------------------------------------------------|
| `set`                     | Displays environment variables.                                                |
| `set <variable_name>=<value>` | Sets an environment variable.                                                |
| `echo %<variable_name>%`  | Prints the value of an environment variable.                                    |

---

### **Advanced Operations**
| Command                                           | Description                                                             |
|---------------------------------------------------|-------------------------------------------------------------------------|
| `wmic process list`                               | Displays a list of processes with more details.                        |
| `wmic process where name="<process_name>" delete` | Terminates a specific process using its name (e.g., `wmic` alternative).|
| `netstat -ano`                                    | Lists active connections with PID details.                             |

---

### **Example Usage**
1. **Kill a process by its PID:**
   ```cmd
   taskkill /PID 1234
   ```

2. **Delete a folder and its content:**
   ```cmd
   rmdir /s /q C:\path\to\folder
   ```

3. **Check disk space and drives:**
   ```cmd
   chkdsk C: /f /r
   ```

4. **Restart the machine immediately:**
   ```cmd
   shutdown /r /t 0
   ```

5. **List the tasks running on the machine:**
   ```cmd
   tasklist
   ```
