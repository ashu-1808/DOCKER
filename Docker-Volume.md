# 📦 Docker Volume
---



## 🔹 Create Docker Volume
```
docker volume create myvol
````

---

## 🔹 List Docker Volumes

```bash
docker volume ls
```

---

## 🔹 Inspect Volume

```bash
docker volume inspect myvol
```

---

## 🔹 Pull Image (Ubuntu)

```bash
docker pull ubuntu
```

---

## 🔹 Create Container & Mount Volume

### Using --mount (recommended)

```bash
docker run -itd --name c1 --mount source=myvol,target=/data ubuntu
```

### Using -v (shortcut)

```bash
docker run -itd --name cont1 -v myvol:/data ubuntu
```

---

## 🔹 List Running Containers

```bash
docker ps
```

---

## 🔹 Login into Container

```bash
docker exec -it c1 /bin/bash
```

---

## 🔹 Navigate to Volume Directory

```bash
cd /data
```

---

## 🔹 Create Files

```bash
touch index.html error.html style.css
```

---

## 🔹 Exit Container

```bash
exit
```

---

## 🔹 Create Second Container with Same Volume

### Using --mount

```bash
docker run -itd --name c2 --mount source=myvol,target=/data2 ubuntu
```

### Using -v

```bash
docker run -itd --name cont2 -v myvol:/data2 ubuntu
```

---

## 🔹 Verify Data Sharing

```bash
docker exec -it c2 /bin/bash
cd /data2
ls
```

👉 You will see:

```
index.html error.html style.css
```

---

## 🔹 Stop Containers

```bash
docker stop c1 c2
```

---

## 🔹 Remove Containers

```bash
docker rm c1 c2
```

---

## 🔹 Check Volume Still Exists

```bash
docker volume ls
```

---

## 🔹 Remove Volume

```bash
docker volume rm myvol
```

---

## 🧠 Key Concept

Docker volumes allow data to persist independently of containers and can be shared across multiple containers.

---

## 🎯 Interview One-Liner

> Docker volumes are used to persist data and share it between containers even after the container is deleted.


