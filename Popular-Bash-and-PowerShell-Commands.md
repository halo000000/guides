# **Comparison of Popular Bash and PowerShell Commands**

| **Bash Command**        | **PowerShell Command**          | **Description**                                                                                    |
|--------------------------|---------------------------------|----------------------------------------------------------------------------------------------------|
| `ls`                    | `Get-ChildItem`                | Lists files and directories in the current directory.                                             |
| `cd <directory>`        | `Set-Location <directory>`     | Changes the current working directory.                                                           |
| `pwd`                   | `Get-Location`                 | Displays the current working directory.                                                          |
| `cp <source> <target>`  | `Copy-Item <source> <target>`  | Copies files or directories.                                                                     |
| `mv <source> <target>`  | `Move-Item <source> <target>`  | Moves or renames files and directories.                                                          |
| `rm <file>`             | `Remove-Item <file>`           | Deletes files or directories.                                                                    |
| `cat <file>`            | `Get-Content <file>`           | Displays the contents of a file.                                                                 |
| `echo <text>`           | `Write-Output <text>`          | Prints text to the console.                                                                      |
| `touch <file>`          | `New-Item <file> -ItemType File` | Creates a new, empty file.                                                                       |
| `mkdir <directory>`     | `New-Item <directory> -ItemType Directory` | Creates a new directory.                                                                         |
| `rmdir <directory>`     | `Remove-Item <directory>`      | Deletes a directory (use `-Recurse` to delete non-empty directories in PowerShell).              |
| `grep <pattern>`        | `Select-String <pattern>`      | Searches for a pattern in files.                                                                |
| `find <path>`           | `Get-ChildItem <path> -Recurse`| Finds files and directories matching a pattern recursively.                                      |
| `man <command>`         | `Get-Help <command>`           | Displays the manual or help for a command.                                                      |
| `history`               | `Get-History`                  | Displays the command history.                                                                   |
| `clear`                 | `Clear-Host`                   | Clears the console screen.                                                                      |
| `chmod <permissions>`   | `icacls`                       | Changes file or directory permissions. (PowerShell uses `icacls` or `Set-Acl` for this purpose.) |
| `ps`                    | `Get-Process`                  | Displays a list of running processes.                                                           |
| `kill <PID>`            | `Stop-Process -Id <PID>`       | Terminates a process by its PID (Process ID).                                                   |
| `df -h`                 | `Get-PSDrive`                  | Displays disk space usage (PowerShell shows drive information with `Get-PSDrive`).              |
| `top`                   | `Get-Process | Out-GridView`   | Displays real-time process information (PowerShell uses commands like `Get-Process` for details).|
| `whoami`                | `whoami` or `$env:USERNAME`    | Displays the current logged-in user.                                                           |
| `env`                   | `Get-ChildItem Env:`           | Displays all environment variables.                                                             |
| `export VAR=value`      | `$env:VAR = "value"`           | Sets an environment variable.                                                                   |
| `alias name='command'`  | `Set-Alias <name> <command>`   | Creates a command alias.                                                                        |
| `scp <source> <target>` | `Copy-Item -ToSession`         | Copies files between local and remote systems (PowerShell uses `PSSession` for remote tasks).    |
| `wget <url>`            | `Invoke-WebRequest <url>`      | Downloads files from a URL.                                                                     |

This table outlines some of the most common commands in Bash and their equivalent in PowerShell, along with a description of their purpose. 