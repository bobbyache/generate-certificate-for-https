# Generate certificate for HTTPS

Files compressed to prevent LF changing to CRLF.

Initially kept to ensure that you could always generate a developer certificate for use  by Angular to run over https.

The `generate.sh` file doesn't work too well on Windows. However, you can run this code in Git Bash:

```
openssl req -newkey rsa:2048 -x509 -nodes -keyout server.key -new -out server.crt -config ./openssl-custom.cnf -sha256 -days 7300
```

You'll run the command from within the repository's root folder.