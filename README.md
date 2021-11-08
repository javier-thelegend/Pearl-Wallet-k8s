# Pearl-Wallet-k8s

Steps:
1. Go to https://console.cloud.google.com/
2. Create new project "pearl-wallet"
3. Go to Kubernets Engine
4. Create cluster GKE Autopilot
5. Open Cloud Shell in a separated Window
  5.1. Clone https://github.com/javier-thelegend/Pearl-Wallet-k8s.git
  5.2. Open as Visual Studio
6. Open repository as Visual Studio
7. Update database.yml as type: ClusterIP and remove NodePort
8. Update pearl-wallet-be.yml as type: LoadBalancer
9. Update pearl-wallet-fe.yml as type: LoadBalancer
10. Apply all yml files and check Workloads in Kubernets, all status should be OK 
11. Check Services & Ingress, all status should be OK, in this tab you will see public endpoints
12. Click on them to check if worked
