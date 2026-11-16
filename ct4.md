1.	Открываем PowerShell не в админе и входим в Убунту
wsl -d Ubuntu
  <img width="536" height="94" alt="image" src="https://github.com/user-attachments/assets/518fd512-ad88-4f40-9e2a-a4375f96b5c6" />

2.	Вводим ноды
export PATH="$HOME/bin:/usr/bin:/bin"
kubectl get nodes            # 3 ноды Ready
kubectl get pods -o wide      # 6 подов nginx Running
kubectl get svc               # nginx-http, nginx-https
<img width="974" height="348" alt="image" src="https://github.com/user-attachments/assets/b2075c46-b0b7-4651-a154-f456d5b56f32" />

3.	Выводим скрипты
bash /mnt/c/Users/thezo/Documents/MultiTool/HomeChats/Chat-7/kind-status.sh   # узлы и сервисы
bash /mnt/c/Users/thezo/Documents/MultiTool/HomeChats/Chat-7/kind-nginx.sh    # пересоздать deployment+сервисы
bash /mnt/c/Users/thezo/Documents/MultiTool/HomeChats/Chat-7/kind-curl.sh     # проверка nginx через curl
<img width="974" height="518" alt="image" src="https://github.com/user-attachments/assets/d4f4f66f-5ab6-4155-8630-6b6720d63a6c" />

4.	Проверка доступа
kubectl run curltest --image=curlimages/curl --rm -it --restart=Never -- curl -s http://10.96.75.98
<img width="974" height="489" alt="image" src="https://github.com/user-attachments/assets/ce3136e6-6a29-4913-af50-68279f7f684e" />
