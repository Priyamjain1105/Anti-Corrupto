# 🛡️ Anti Corrupto

## Overview

In today's governance landscape, **transparency** and **accountability** are indispensable for fostering trust and combating corruption. Manual processes and opaque systems often facilitate malfeasance, leading to public disillusionment. This project addresses these challenges by harnessing innovative technologies, notably **blockchain** and **analytics**, to revolutionize governance practices.

### Key Features

- **Blockchain-Powered Systems**: Implement automated traffic monitoring and automated challan systems through edge computing and a secure land registry to establish tamper-proof records, minimizing corruption opportunities.

- **Smart Contracts**: Automate processes such as ticketing and fund allocation to reduce bribery risks.

- **Secure Whistleblower Platform**: Foster accountability and provide a secure way for whistleblowers to report misconduct.

- **Data-Driven Insights**: Enable efficient resource allocation through analytics.

### Goals

This platform not only encourages transparency but also fosters a culture of accountability within governmental institutions. By addressing issues in land registry, such as stamp duty evasion and undervaluation, the project aims to restore public trust in governmental systems. It sets a precedent for responsible and effective administration, ultimately fostering a more equitable and just society.

---

## 🚀 How to Run the Project

### 1. Run PostgreSQL Database

  - **Start the database**:
    ```bash
    docker-compose up
    ```
  - **Access the database container**:
    ```bash
    docker exec -it <container_id> /bin/bash
    ```
  
### 2. Run the Backend
  - **Install dependencies:**
    ```bash
      npm install
    ```
  - **Migrate the database:**
    ```bash
    npx prisma migrate dev
    ```
  - **Generate Prisma client:**
    ```bash
    npx prisma generate
    ```
  - **Launch Prisma Studio:**
    ```bash
    npx prisma studio
    ```

### 3. Eun the Mobile Frontend
  - **Install dependencies:**
    ```bash
    npm install
    ```
  - **Start Expo Server:**
    ```bash
    npx expo start
    ```
  - **Run on Device**
    - Press `a ` for Android
    - Press `i` for IOS

### 4. Environment Variables
  Ensure you have a `.env` file with the following content:
  ```env
  DATABASE_URL=postgresql://postgres:123@db:5432/capstone?schema=public
  ACCESS_TOKEN_PRIVATE_KEY=
  REFRESH_TOKEN_PRIVATE_KEY=
  PORT=3000
  ```

### 5. Run the ML Model
- **Install Python dependencies:**
  ```bash
  pip3 install -r requirements.txt
  ```
- **Execute the model:**
  ```bash
  python main.py
  ```
  
### 6. Deploy Smart Contracts
- Deploy contracts using Hardhat:
```bash
npx hardhat run scripts/deploy.js --network sepolia
```
- Get ABI in artifacts.
