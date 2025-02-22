# LuxeTrack 🚀  
*A DApp for tracking luxury goods on the blockchain.*  

LuxTrack ensures authenticity and secure ownership transfer of luxury items by leveraging smart contracts and blockchain technology. With LuxeTrack, manufacturers, sellers, and buyers can verify product authenticity, prevent counterfeiting, and maintain a transparent ownership history.  

## Features  
✅ **Secure Item Registration** – Store luxury item details immutably on the blockchain.  
✅ **Ownership Tracking** – Seamless and verifiable ownership transfers.  
✅ **Real-time Authentication** – Buyers can verify authenticity via blockchain records.  
✅ **Decentralized & Transparent** – No central authority; trust is built on blockchain.  

## Tech Stack  
- **Blockchain**: Ethereum  
- **Smart Contracts**: Solidity  
- **Frontend**: React.js
- **Backend**: Node.js

✔ Simple Ownership Tracking – Items are stored as structured data instead of tokens.<br>
✔ Easy Integration – Works well for businesses that don’t need NFTs.

## 🏗 System Architecture  

### **1️⃣ Frontend (React.js / Next.js)**  
- Provides the **UI** for:  
  ✅ Item registration  
  ✅ Ownership transfers  
  ✅ Verification of authenticity  
- Connects to the backend.  

### **2️⃣ Backend (Node.js)**
🔹 **Role:** Acts as the **business logic layer** and off-chain data store.  

- Stores **off-chain metadata** (luxury item details) in **MongoDB**.  
- Provides **REST API** for frontend interactions.  
- Handles **authentication & user roles** (manufacturer, seller, buyer).  
- Manages **QR code generation** for item verification.  
- **Interacts with the blockchain** for contract execution.  
- Implements **rate limiting and security** features.  

### **3️⃣ Smart Contracts (Solidity on Ethereum)**  
🔹 **Role:** Ensures secure & immutable luxury item tracking.  

- **Item Registration Contract:**  
  ✅ Stores core item details on-chain (serial number, manufacturer, etc.).  
- **Ownership Transfer Contract:**  
  ✅ Manages verified ownership transfers.  
- **Verification Mechanism:**  
  ✅ Allows anyone to check an item’s authenticity via its **Item ID**.  

### **4️⃣ Blockchain (Ethereum)**
- Stores **on-chain luxury item records** and **ownership history**.  

### **5️⃣ Storage (MongoDB)**  
- **MongoDB**:  
  ✅ Stores **business-related metadata** (e.g., warranty info, resale value, etc.).  
  ✅ Stores **user profiles & access roles**.  
- **IPFS (Optional):**  
  ✅ Stores large files (product images, certificates).  

---

## 🔄 Workflow: How It Works  

### **1️⃣ Step 1: Item Registration**
- Manufacturer submits item details via the **frontend**.  
- The **backend**:  
  ✅ Stores extra metadata in **MongoDB**.  
  ✅ Calls the **smart contract** to register the item on-chain.  
  ✅ Generates and stores a **QR code** linked to the item.  

### **2️⃣ Step 2: Ownership Transfer**
- When the item is sold, the **backend API** validates the transaction.  
- The **smart contract** updates the owner on-chain.  
- The **backend updates its own database** for off-chain records.  

### **3️⃣ Step 3: Verification & Authentication**
- A buyer scans the **QR code** or enters the **Item ID**.  
- The **frontend** calls the **backend API**, which:  
  ✅ Fetches on-chain ownership history.  
  ✅ Retrieves **metadata** (if stored off-chain).  
- The frontend displays the **authenticity report**.  

📜 Licensed under the **MIT License**  
