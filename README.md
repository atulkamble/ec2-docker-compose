## 📌 Clean Reinstall of Docker Compose on Amazon Linux / EC2

### 1️⃣ Remove old docker-compose if it exists:

```bash
sudo rm -f /usr/local/bin/docker-compose
```

### 2️⃣ Install Docker Compose V2 plugin:

If Docker is already installed:

```bash
sudo mkdir -p /usr/local/lib/docker/cli-plugins
sudo curl -SL https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64 -o /usr/local/lib/docker/cli-plugins/docker-compose
sudo chmod +x /usr/local/lib/docker/cli-plugins/docker-compose
```

Check for the latest release [here](https://github.com/docker/compose/releases).

---

### 3️⃣ Verify installation:

```bash
docker compose version
```

Notice — with V2 it’s `docker compose` (space) not `docker-compose` (hyphen) anymore.

---

### 4️⃣ Now run your project:

```bash
docker compose up --build
```
