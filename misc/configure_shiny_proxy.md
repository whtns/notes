# how to configure public seuratTools shiny app
1. visit webserver at cobriniklab.saban-chla.usc.edu
2. configure Dockerfile in seuratToolsImage
```# copy the app to the image
RUN mkdir /root/seuratApp
COPY reintegration_test /root/seuratApp 
```
3. edit /etc/shinyproxy/application.yml to ensure the right docker volume is mounted
4. run `systemctl status shinyproxy` and `sudo systemctl restart shinyproxy` to rebuild the app after editing the Dockerfile
