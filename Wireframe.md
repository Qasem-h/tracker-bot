

### **Wireframe for Dashboard (Core Backend)**

#### **1.1 User Management**
- **Components**: 
  - List of registered users (filter by platform: Telegram, Discord, Website).
  - Search bar to find users by username or wallet.
  - User activity status (Active, Inactive).
  - Option to manage user alerts, track wallets, and remove users.

- **Key Actions**:
  - View user details (platform, wallet addresses, alert types).
  - Assign or remove wallets manually.
  - Delete a user or transfer data to another platform.

#### **1.2 Wallet Tracking System**
- **Components**:
  - List of wallets being tracked (sorted by user).
  - Filter by blockchain (Ethereum, Solana, Binance Smart Chain).
  - Last transaction date and time, balance status.

- **Key Actions**:
  - Add or remove wallets from the user.
  - Link wallet to multiple alert types (transaction, price).
  - Check wallet history and balance changes.

#### **1.3 Alert Configuration**
- **Components**:
  - List of all alerts (sorted by user and alert type).
  - Alert status (Active, Paused, Expired).
  - Alert types (Price, Transaction, Balance).

- **Key Actions**:
  - Set or modify alert parameters (e.g., price thresholds).
  - Assign alerts to a specific wallet.
  - Manage alert delivery methods (Telegram, Discord, etc.).
  - Pause or delete alerts.

#### **1.4 Platform Management**
- **Components**:
  - Platforms linked to the bot (Telegram, Discord, Website).
  - Integration status (Connected, Disconnected).
  - Platform user count.

- **Key Actions**:
  - Manage integration settings (API keys, webhook configurations).
  - Sync user data between platforms.
  - Test alerts or wallet tracking across platforms.

---

### **Wireframe for Telegram Bot**

#### **2.1 User Registration Flow**
- **Flow**:
  - User sends `/start` command to begin.
  - Bot responds with a welcome message and instructions to register their wallet.
  - Bot asks for the user’s preferred blockchain and wallet address.

- **Components**:
  - Registration flow that captures platform type (Telegram).
  - Ability to ask for wallet addresses from multiple blockchains.

- **Key Actions**:
  - Register user with wallet and platform details.
  - Save user preferences and notify them of successful registration.

#### **2.2 Wallet Tracking & Alert Setup**
- **Flow**:
  - User sends `/addwallet` to add a new wallet for tracking.
  - Bot prompts for blockchain and wallet address.
  - User confirms the wallet and selects alert types (price, transaction, balance changes).

- **Components**:
  - Menu-driven conversation for setting alerts (e.g., price threshold or transaction type).
  - Show active wallets and alerts with options to modify or delete them.

- **Key Actions**:
  - Set up wallet-specific alerts for price changes, transaction alerts.
  - Notify the user when an alert is triggered.
  - User can manage (pause/delete) active alerts directly through the bot.

#### **2.3 Multi-Platform Link**
- **Flow**:
  - User can link their Telegram account to Discord or the Website for unified management.
  - Bot sends a link to authenticate on other platforms.

- **Components**:
  - Link generation and sharing for Discord or Website sign-up.
  - Syncing wallets and alerts between platforms.

- **Key Actions**:
  - Notify the user when their Telegram, Discord, and Website accounts are linked.
  - Provide user the ability to view and manage data across platforms.

---

### **Core Backend Components**

#### **3.1 User Data Storage**
- **Data Fields**:
  - User ID, Username, Platform (Telegram, Discord, Website).
  - Wallet addresses (linked to the user).
  - Active alerts (type, status).
  
- **Key Functions**:
  - Register and track multiple wallets per user.
  - Link user data across multiple platforms (Telegram, Discord).

#### **3.2 Wallet Alert System**
- **Components**:
  - Alert trigger mechanisms for price, transactions, and balance changes.
  - Cross-platform notification system (Telegram, Discord, Email).
  
- **Key Functions**:
  - Trigger alerts based on blockchain activity (real-time checks).
  - Push notifications to linked platforms (Telegram, Discord).

---
