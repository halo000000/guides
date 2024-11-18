### **Protocols Explained**

#### **1. FTP (File Transfer Protocol)**  
**Purpose**: FTP is used to transfer files between a client and a server over a network.

**How to Use FTP in the Command Line**:  
1. **Connect to an FTP server**:
   ```bash
   ftp <server-address>
   ```
   Example:  
   ```bash
   ftp ftp.example.com
   ```
2. **Log in**: Enter your username and password when prompted.
3. **Common Commands**:
   - `ls` or `dir`: List files on the server.
   - `cd <directory>`: Change directory on the server.
   - `get <file>`: Download a file from the server.
   - `put <file>`: Upload a file to the server.
   - `quit`: Exit the FTP session.
4. **Secure Alternative**: Use SFTP (SSH-based) for encrypted file transfers:
   ```bash
   sftp <username>@<server-address>
   ```

---

#### **2. HTTP (Hypertext Transfer Protocol)**  
**Purpose**: HTTP is used for transferring web pages and data between clients (browsers) and servers.  

**How to Use HTTP in the Command Line**:  
1. **Send a GET request** using `curl` or `wget`:
   ```bash
   curl http://example.com
   wget http://example.com
   ```
2. **Send a POST request** with data:
   ```bash
   curl -X POST -d "key=value" http://example.com/api
   ```
3. **Inspect HTTP Headers**:
   ```bash
   curl -I http://example.com
   ```
   This returns the HTTP headers only, such as the status code, content type, etc.

---

#### **3. SSH (Secure Shell)**  
**Purpose**: SSH is used to securely log into remote systems and execute commands or manage files over an encrypted connection.  

**How to Use SSH in the Command Line**:  
1. **Log into a remote system**:
   ```bash
   ssh <username>@<server-address>
   ```
   Example:
   ```bash
   ssh user@192.168.1.10
   ```
2. **Specify a Port**:
   ```bash
   ssh -p <port> <username>@<server-address>
   ```
   Example:
   ```bash
   ssh -p 2222 user@example.com
   ```
3. **Copy files over SSH (SCP)**:
   ```bash
   scp <file> <username>@<server-address>:<destination-path>
   ```
   Example:
   ```bash
   scp file.txt user@192.168.1.10:/home/user/
   ```
4. **SSH Configuration File**:
   Simplify connections by editing `~/.ssh/config` to save server details.

---

#### **4. SMTP (Simple Mail Transfer Protocol)**  
**Purpose**: SMTP is used for sending email messages between servers or from a client to a server.

**How to Use SMTP in the Command Line**:  
1. **Use `telnet` or `netcat` for testing SMTP servers**:
   ```bash
   telnet <smtp-server-address> 25
   ```
   Example:
   ```bash
   telnet smtp.example.com 25
   ```
   Steps:
   - Send the `HELO` command:
     ```plaintext
     HELO example.com
     ```
   - Specify the sender:
     ```plaintext
     MAIL FROM:<sender@example.com>
     ```
   - Specify the recipient:
     ```plaintext
     RCPT TO:<recipient@example.com>
     ```
   - Input the email body:
     ```plaintext
     DATA
     Subject: Test Email
     This is a test email.
     .
     ```
   - Quit:
     ```plaintext
     QUIT
     ```
2. **Send email using `sendmail`**:
   ```bash
   echo "Subject: Test Email" | sendmail recipient@example.com
   ```
3. **Use `msmtp` or `swaks` for more advanced email sending**:
   Example with `swaks`:
   ```bash
   swaks --to recipient@example.com --server smtp.example.com --auth-user user@example.com --auth-password password
   ```

---

### **Summary Table**

| **Protocol** | **Purpose**                                    | **Command Line Example**                                                                 |
|--------------|------------------------------------------------|------------------------------------------------------------------------------------------|
| **FTP**      | File transfer                                  | `ftp ftp.example.com`                                                                    |
| **HTTP**     | Web page and data transfer                     | `curl -X GET http://example.com`                                                        |
| **SSH**      | Secure remote login and command execution      | `ssh user@192.168.1.10`                                                                 |
| **SMTP**     | Sending email                                  | `telnet smtp.example.com 25` or `echo "Subject: Test" | sendmail recipient@example.com` |
