# K8s_Probes

### Probes -
- To investigate or monitor something and to take necessary actions

### Health Probes -
- Health probes monitor your Kubernetes applications and take necessary actions to recover from failure
- To ensure your application is highly available and self-healing

### Type of health probes in Kubernetes
- Readiness ( Ensure application is ready)
- Liveness ( Restart the application if health checks fail)
- Startup ( Probes for legacy applications that need a lot of time to start)

---
## Liveness on a File

`kind create cluster --name=pavantest --config=kind-cluster-nodes.yml` 

`k apply -f liveness-file.yaml`

`k get pods -w`

![image](https://github.com/user-attachments/assets/d92032be-b14b-414b-a5a6-c19f76a568b6)

`k describe pod liveness-exec`

![image](https://github.com/user-attachments/assets/a0b75b00-9cfc-46b5-8d84-7de0cd02db5f)

---

## Liveness using HTTP

`k apply -f liveness-http.yaml`

`k exec -it hello -- sh`

![image](https://github.com/user-attachments/assets/c4773245-c247-4f00-884f-406a32989cf6)

`k get pods -w`

![image](https://github.com/user-attachments/assets/0a411981-b6c6-483b-a0f2-946d2048ac87)

`k describe pod hello`

![image](https://github.com/user-attachments/assets/95054c9b-111e-4d60-9102-6358d080f072)

---

## Liveness using TCP


`k apply -f liveness-tcp.yaml`

`k get pods -w`

![image](https://github.com/user-attachments/assets/610d1b10-c075-4c6f-8853-f67272616af5)

