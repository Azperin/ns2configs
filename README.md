### Как юзать в юните


```[Unit]
Description=NS2 Server 1
After=network.target

[Service]
WorkingDirectory=/home/ns2server/serverfiles/x64/
ExecStart=/home/ns2server/serverfiles/x64/server_linux -file "/home/ns2server/.config/ns2configs/server1/command_line.txt"
Restart=on-failure
RestartSec=30s
User=ns2server
Group=ns2server

[Install]
WantedBy=multi-user.target```