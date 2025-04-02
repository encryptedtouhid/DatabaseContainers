## 🚀 Running Azure Cosmos DB Emulator (Docker)

The Azure Cosmos DB Emulator provides a local environment that emulates the Azure Cosmos DB service for development and testing purposes.

> ⚠️ Note: The emulator works on Windows or Linux with Docker (WSL2/Hyper-V support required).

---

### 🛠️ How to Run

1. **Ensure Docker is installed and running**.

2. **Start the Cosmos DB Emulator** using Docker Compose:

   ```bash
   docker-compose up -d cosmosdb

Or using a one-liner Docker command:

```bash
docker run -p 8081:8081 -p 10251-10255:10251-10255 \
  --name=cosmosdb-emulator \
  -e AZURE_COSMOS_EMULATOR_PARTITION_COUNT=1 \
  -e AZURE_COSMOS_EMULATOR_ENABLE_DATA_PERSISTENCE=true \
  -e AZURE_COSMOS_EMULATOR_IP_ADDRESS_OVERRIDE=127.0.0.1 \
  -it mcr.microsoft.com/cosmosdb/linux/azure-cosmos-emulator

  
### 🔑 Get the Emulator Master Key

To retrieve the master key (required for connecting to the emulator), run the following command:

```bash
docker exec cosmosdb-emulator /get-master-key.sh

This will output a long string — your primary key — which is needed to authenticate with the emulator.

### 🌐 Connect to the Emulator

- **Endpoint**: `https://localhost:8081`
- **Primary Key**: Use the key retrieved from `/get-master-key.sh`
- ⚠️ The emulator uses a **self-signed SSL certificate**:
  - In **local development**, SDKs may require disabling SSL verification or trusting the certificate.
  - In **browsers or Postman**, you may need to manually accept the certificate exception.

---

### ✅ Example Connection String (SQL API)

```plaintext
AccountEndpoint=https://localhost:8081/;
AccountKey=<your-master-key>;

Replace <your-master-key> with the actual key retrieved via Docker.