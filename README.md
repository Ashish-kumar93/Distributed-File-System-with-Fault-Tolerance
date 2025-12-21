# 📁 Distributed File System with Fault Tolerance

A **Python-based Distributed File System (DFS)** that splits files into chunks, distributes them across multiple storage nodes, and ensures **fault tolerance using replication**.  
This project simulates real-world distributed systems such as **Google File System (GFS)** and **HDFS**.

---

## 📌 Project Overview

The Distributed File System allows users to upload and download files in a distributed environment. Files are divided into fixed-size chunks, stored across multiple storage nodes, and replicated to prevent data loss during node failures. A centralized **Master Node** manages metadata and coordinates communication between clients and storage nodes.

---

## ✨ Key Features

- Chunk-based file storage  
- Centralized metadata management  
- Multiple independent storage nodes  
- Replication for fault tolerance  
- Node failure simulation  
- Seamless file download during failures  
- Logging for monitoring and debugging  
- Configurable chunk size and replication factor  

---

## 🏗 System Architecture

Client → Master Node → Storage Nodes  
Metadata is stored centrally, while actual file chunks are distributed.

---

## 🔁 Working Flow

### Upload Process
1. Client selects a file  
2. File is split into chunks  
3. Client requests node allocation from Master  
4. Master assigns storage nodes and replicas  
5. Chunks are uploaded to storage nodes  
6. Metadata is updated  

### Download Process
1. Client requests file  
2. Master returns chunk locations  
3. Client downloads chunks  
4. Replicas are used if a node fails  
5. File is reconstructed  

---

## 🛠 Technologies Used

### Programming Language
- Python 3.x

### Libraries & Tools
- socket
- threading
- json
- os, shutil
- hashlib
- logging

### Other Tools
- Git & GitHub
- VS Code / PyCharm
- Command Line / Terminal

---

## 📂 Project Structure

DistributedFileSystem/
├── master.py
├── node.py
├── client_app.py
├── utils.py
├── config.py
├── start_cluster.py
├── dfs_metadata.json
├── dfs_storage/
├── logs/
└── README.md

---

## 🚀 How to Run the Project

### Clone Repository
```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### Start Cluster
```bash
python start_cluster.py
```

### Run Client
```bash
python client_app.py
```

---

## 🧪 Testing

- Upload and download files  
- Simulate node failure  
- Verify replica usage  
- Monitor logs  

---

## 🔮 Future Scope

- Automatic re-replication  
- Load balancing  
- Data encryption  
- Web-based dashboard  
- Docker deployment  

---

## 👨‍💻 Contributors

(Add your details here)

---

## 📄 License

Academic Project – Free to use for learning purposes.
