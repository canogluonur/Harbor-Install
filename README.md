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
