# gfw_script
Copy the file into `/etc/systemd/sytstem` and the run the command lines:
```
sudo apt update
sudo apt full-upgrade -y
sudo apt install shadowsocks-libev simple-obfs
sudo systemctl daemon-reload
sudo systemctl enable obfs-80.service obfs-443.service obfs-8080.service shadowsocks-libev-8964.service
sudo systemctl start obfs-80.service obfs-443.service obfs-8080.service shadowsocks-libev-8964.service
```

Now you have gotten a shadowsocks server with port 8964 and three obfs-server in the port 80,443 and 8080. All of the servers have the same password and encrypt method.

The obfs method for 80 port is `http`

The obfs method for 443 port is `tls`

The obfs method for 8080 port is `http`

PS: If you are using Ubuntu, maybe you have to modify the `obfs-server` path in the `obfs-*` files
