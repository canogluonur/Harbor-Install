# Harbor-Install-On-Docker 
Harbor is an open-source Container Registry. Harbor Installation On Docker step one step.
```
tar xzvf harbor-online-installer-version.tgz
cd harbor
sudo nano  harbor.yml
```
```
set hostname : registry.xxx.com
```
```
close https configuration
```
```
set external_url:  https://registry.xxx.com
```
```
set data_volume:/data/docker-volumes/harbor
```

save and quit
```
run ./install.sh
```
It’s okey. You can go to your url “http://registry.xxx.com"


You also see this error if Harbor uses HTTPS with an unknown CA certificate. In this case, obtain the registry’s CA certificate, and copy it to /etc/docker/certs.d/myregistrydomain.com/ca.crt.


if you get an "unknown blob" error on pull and push commands. 
```
cd harbor
vi docker-compose.yml
add the registry service's env:
    environment:
      - REGISTRY_HTTP_RELATIVEURLS=true
```
