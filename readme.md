# 🐳 Docker Compose Configurations

This repository contains Docker Compose (`docker-compose.yml`) files for running popular databases locally using Docker. These setups are ideal for development and testing purposes.

---

## 📦 Available Services

| Database      | Description                                         | Port(s)     | Credentials                          |
|---------------|-----------------------------------------------------|-------------|---------------------------------------|
| MongoDB       | NoSQL database with admin user                     | `27017`     | `mongoadmin` / `password`             |
| MySQL         | Relational DB with custom user & DB                | `3306`      | `root` / `password`, `myadmin`     |
| SQL Server    | Microsoft SQL Server Express edition               | `1433`      | `sa` / `password`                     |
| Cosmos DB     | Azure Cosmos DB Emulator for local development     | `8081`      | Use `/get-master-key.sh` in container |
| Oracle XE     | Oracle 21c Express Edition                         | `1521`, `5500` | `SYS` / `password`                   |

---

## 🛠️ Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/encryptedtouhid/DatabaseContainers.git
   cd FolderName

2. Navigate to the specific folder (if split) or just run:
   ```bash
   docker-compose up -d

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

- 📄 Add support for more databases (e.g., PostgreSQL, Redis, Neo4j)
- 🛡️ Improve security, configuration, or compatibility
- 📚 Enhance documentation with usage tips or code examples
- 🧪 Add integration tests (where applicable)


### Steps to contribute:

1. **Fork** this repository to your GitHub account.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/your-username/docker-db-stacks.git
   cd docker-db-stacks
3. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
4. Make your changes, then commit:
   ```bash
   git add .
   git commit -m "Add: description of your change"
5. Push to your fork:
   ```bash
   git push origin feature/your-feature-name

6. **Open a Pull Request on GitHub**:

   - Go to your fork on GitHub
   - Click **“Compare & pull request”**
   - Add a **clear title** and **detailed description** explaining your changes
   - Link any relevant issues (e.g., `Closes #12`)
   - Click **“Create pull request”**

---

✅ **PR Tips:**

- Keep pull requests focused and minimal — one purpose per PR
- Test your changes locally before submitting
- Follow the coding and naming conventions used in the project
- If you’re unsure about something, open a draft PR or ask in the issues!

---

Thank you for contributing — every improvement counts! 🎉



   
