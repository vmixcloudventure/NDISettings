# NDISettings
NDISettings for zoom instances




NDI SDK works well on Ubuntu server 1804
Just download the link (wget) extract, (tar -xf) and run
created a systemctl service for it
Store this unit under /etc/systemd/system/ndidisco.service

[Unit]
Description=NDIDiscoServer

[Service]
ExecStart=/home/ubuntu/SDK/bin/x86_64-linux-gnu/ndi-directory-service

[Install]
WantedBy=multi-user.target

$ sudo systemctl daemon-reload
Start the service with:

$ sudo systemctl start ndidisco.service
And enable it during startup with:

$ sudo systemctl enable ndidisco.service
You can check the status of the service with:

$ systemctl status ndidisco.service
