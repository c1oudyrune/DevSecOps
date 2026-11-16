1.
Start-Process "C:\Program Files\Docker\Docker\Docker Desktop.exe"
<img width="679" height="111" alt="image" src="https://github.com/user-attachments/assets/b4b8a652-c614-4fdc-875b-9421598120c5" />

2.
docker start onlyoffice-documentserver
<img width="463" height="32" alt="image" src="https://github.com/user-attachments/assets/a7984dc8-4600-452e-a591-2c465d25adf6" />

3.
docker ps
<img width="839" height="160" alt="image" src="https://github.com/user-attachments/assets/91ca1197-3a6a-4c0a-a8b7-ab621550341a" />

4.
docker rm -f onlyoffice-documentserver
docker run -d -p 8080:80 -v onlyoffice_data:/var/www/onlyoffice/Data -v onlyoffice_logs:/var/log/onlyoffice -v onlyoffice_cache:/var/lib/onlyoffice/documentserver/App_Data/cache --name onlyoffice-documentserver onlyoffice/documentserver:latest
<img width="833" height="190" alt="image" src="https://github.com/user-attachments/assets/e3947f3f-ce6b-4416-9b15-bfb3f4219d23" />
Если что либо сломалось
docker rm -f onlyoffice-documentserver
docker run -d -p 8080:80 -v onlyoffice_data:/var/www/onlyoffice/Data -v onlyoffice_logs:/var/log/onlyoffice -v onlyoffice_cache:/var/lib/onlyoffice/documentserver/App_Data/cache --name onlyoffice-documentserver onlyoffice/documentserver:latest


http://localhost:8080/welcome/
<img width="1649" height="843" alt="image" src="https://github.com/user-attachments/assets/6e802717-4489-44f8-b457-5d685768f470" />
