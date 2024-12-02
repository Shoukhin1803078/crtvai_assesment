# Flask Chatbot with MySQL Integration

Here I give an overview what I understand for this task:
## 📋 Overview

This chatbot application demonstrates:
- Custom session management using MySQL
- Multi-user conversation handling
- Persistent conversation states
- Real-time web interface
- Stateful conversation flow

## 🏗️ Architecture

### Backend Components
- **Flask Server**: Handles HTTP requests and session management
- **MySQL Database**: Stores user sessions and conversation states
- **State Machine**: Manages conversation flow

### Database Schema
```sql
CREATE TABLE user_sessions (
    phone_number VARCHAR(20) PRIMARY KEY,
    user_name VARCHAR(100),
    favorite_song VARCHAR(200),
    conversation_state VARCHAR(50),
    last_interaction TIMESTAMP
);
```



## 🚀 Installation

### Prerequisites
- Python 3.8+
- MySQL Server
- pip (Python package manager)


### Step 2: Set Up Virtual Environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Unix/MacOS
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install flask mysql-connector-python
```

### Step 4: Database Setup
1. Install MySQL if not already installed
2. Create database:
```sql
CREATE DATABASE crtvai_db;
```
3. Configure database connection in `app.py`:
```python
db_config = {
    'host': 'localhost',
    'user': 'root',
    'password': '',
    'database': 'crtvai_db'
}
```

## 🎯 Running the Application

1. **Start MySQL Server**

2. **Run Flask Application**
```bash
python app.py
```





# Output from my side :
<img width="1710" alt="Screenshot 2024-12-02 at 3 03 48 PM" src="https://github.com/user-attachments/assets/da6ef8da-c5ae-47fa-aa14-414cccfe2407">
<img width="1710" alt="Screenshot 2024-12-02 at 3 03 07 PM" src="https://github.com/user-attachments/assets/ee20b632-174e-493d-b81d-14df35aa746f">
<img width="1710" alt="Screenshot 2024-12-02 at 3 02 24 PM" src="https://github.com/user-attachments/assets/fbdbbb33-601a-4f1f-8d3c-7011bf358637">
<img width="1710" alt="Screenshot 2024-12-02 at 3 02 13 PM" src="https://github.com/user-attachments/assets/3dade73b-f47b-439b-a990-37bac2500fde">


