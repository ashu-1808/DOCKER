# 📦 Docker Volume
---


# Docker Volume

## 1. Create Docker Volume
docker volume create myvol

## 2. List Volumes
docker volume ls

## 3. Inspect Volume
docker volume inspect myvol

---

## 4. Pull Image
docker pull ubuntu

---

## 5. Create Container & Mount Volume

# Using --mount (recommended)
docker run -itd --name c1 --mount source=myvol,target=/data ubuntu

# Using -v (shortcut)
docker run -itd --name cont1 -v myvol:/data ubuntu

---

## 6. Check Running Containers
docker ps

---

## 7. Login into Container
docker exec -it c1 /bin/bash

---

## 8. Go to Mounted Directory
cd /data

---

## 9. Create Files
touch index.html error.html style.css

---

## 10. Exit Container
exit

---

## 11. Create Another Container Using Same Volume

docker run -itd --name c2 --mount source=myvol,target=/data2 ubuntu

# OR
docker run -itd --name cont2 -v myvol:/data2 ubuntu

---

## 12. Verify Data Sharing

docker exec -it c2 /bin/bash

cd /data2
ls

# You will see:
index.html error.html style.css

---

## 13. Stop Containers
docker stop c1 c2

---

## 14. Remove Containers
docker rm c1 c2

---

## 15. Volume Still Exists (Important Concept)
docker volume ls

---

## 16. Remove Volume
docker volume rm myvol

## 🧠 Key Concept

Docker volumes allow data to persist independently of containers and can be shared across multiple containers.

---

## 🎯 Interview One-Liner

> Docker volumes are used to persist data and share it between containers even after the container is deleted.


