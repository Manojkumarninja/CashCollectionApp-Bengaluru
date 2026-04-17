# 💰 BLR Cash Collection App

A Streamlit app for Bengaluru Ops Executives to update payment collection status per delivery order.

## Features

- **Login** — Secure email & password with facility-level access restriction
- **Update Collection** — Select Date → Facility → Mode → Driver → update each customer
- **Per-customer entry** — Payment Status (Paid / Not Paid) and Collection Window
- **Summary cards** — Total, Updated, Pending, Invoice & Cash totals
- **View Records** — Customer-wise detail and Driver-wise summary with CSV downloads

## Setup

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Configure Secrets
Create a `.env` file:
```env
DB_HOST=your_host
DB_PORT=your_port
DB_USER=your_user
DB_PASSWORD=your_password
DB_NAME=your_database
```

### 3. Run Locally
```bash
streamlit run app.py
```

### 4. Deploy on Streamlit Cloud
Add secrets under **Settings → Secrets**:
```toml
DB_HOST = "your_host"
DB_PORT = "your_port"
DB_USER = "your_user"
DB_PASSWORD = "your_password"
DB_NAME = "your_database"
```

## Database Table
**`FnVCashCollectionBengaluru`** — Pre-populated with delivery order data. App updates `PaymentStatus` and `CollectionWindow` columns.
