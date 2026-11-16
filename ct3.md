1.
uid=999(prometheus) gid=986(prometheus) groups=986(prometheus)
prometheus:x:999:986::/home/prometheus:/sbin/nologin
prometheus, version 2.53.2
<img width="942" height="418" alt="image" src="https://github.com/user-attachments/assets/f983ee92-99a1-49b4-be70-5e113556c39a" />

2.
/usr/local/bin/prometheus, promtool               → prometheus:prometheus
/etc/prometheus/{consoles, console_libraries, prometheus.yml} → prometheus:prometheus
/var/lib/prometheus                              → prometheus:prometheus
<img width="898" height="130" alt="image" src="https://github.com/user-attachments/assets/86d09d84-ee14-4417-bd82-5d049de405a5" />

3.
  prometheus.service - Prometheus
   Loaded: loaded (/etc/systemd/system/prometheus.service; enabled)
   Active: active (running) since Sun 2026-11-15 17:52:17 MSK
автозагрузка: enabled
порт: LISTEN *:9090 (prometheus)
<img width="826" height="178" alt="image" src="https://github.com/user-attachments/assets/6a563d59-84a2-44e5-91ac-ced1a10d3437" />

4.
http://127.0.0.1:9090/graph → HTTP 200
API: {"status":"success", ...}
<img width="537" height="123" alt="image" src="https://github.com/user-attachments/assets/1d2e45a7-ed2b-4187-b6bf-d472ad8ad8aa" />

5.
Status: active
To          Action      From
9090/tcp    ALLOW IN    Anywhere
9090/tcp(v6) ALLOW IN   Anywhere (v6)
<img width="548" height="178" alt="image" src="https://github.com/user-attachments/assets/af96458d-5cc2-4255-a697-93273ca4c8dc" />


http://127.0.0.1:9090/

<img width="1916" height="635" alt="image" src="https://github.com/user-attachments/assets/9577a3a5-d31a-4e64-9f30-b0fa8455d1cc" />

<img width="1303" height="468" alt="image" src="https://github.com/user-attachments/assets/7978d882-53d3-46ea-9a39-9c61605bafa6" />

{job="prometheus"}
