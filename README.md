#Gmail Account
User: test.gcpReact2021@gmail.com
Pass: 70323941

# Pearl-Wallet-k8s

Steps:
1. Go to https://console.cloud.google.com/
2. Create new project "pearl-wallet"
3. Go to Kubernets Engine
4. Create cluster GKE Autopilot
5. Open Cloud Shell in a separated Window
5.1. Clone https://github.com/javier-thelegend/Pearl-Wallet-k8s.git
5.2. Open as Visual Studio
5.3 Connect Terminal Visual Studio with GCP
5.3.1 Go to Kubernets Engine
5.3.2 Clusters
5.3.3 Actions and Connect
5.3.4 Copy Command Line Access
5.3.5 Paste it in Visual Studio Terminal
5.3.6 Clic on Authorize button in Popup
6. Open repository as Visual Studio
7. Update database.yml as type: ClusterIP and remove NodePort
8. Update pearl-wallet-be.yml as type: LoadBalancer
9. Update pearl-wallet-fe.yml as type: LoadBalancer
10. Apply all yml files and check Workloads in Kubernets, all status should be OK 
11. Check Services & Ingress, all status should be OK, in this tab you will see public endpoints
12. Click on them to check if worked

**#Update FE Image with .env**
1. Add .env file with GCP BE host
2. Build new image
3. Push to docker.hub repository
4. Repeat process to deploy in kubernets
5. If this does not work try to create another repo and repeat

**Connect to Postgres**
1. Change yml to type: LoadBalancer
2. Use external ip to connect using dbeaver
3. Import data
4. Rollback yml change
