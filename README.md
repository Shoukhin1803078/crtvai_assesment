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

<img width="1710" alt="Screenshot 2024-12-02 at 5 07 38 PM" src="https://github.com/user-attachments/assets/8ad92069-e8ba-45d3-be2c-fe2885b93f58">
<img width="1710" alt="Screenshot 2024-12-02 at 5 11 42 PM" src="https://github.com/user-attachments/assets/d36ac52e-9d49-4e60-8776-0006c6dbebd5">
<img width="1710" alt="Screenshot 2024-12-02 at 5 13 05 PM" src="https://github.com/user-attachments/assets/66e08095-dba6-4df2-b873-b9227811f205">
<img width="1710" alt="Screenshot 2024-12-02 at 5 14 07 PM" src="https://github.com/user-attachments/assets/b0f40d0f-3c5c-4dcf-b3fa-18e8f2cd7d0e">
<img width="1710" alt="Screenshot 2024-12-02 at 5 14 30 PM" src="https://github.com/user-attachments/assets/a6b79235-439a-43bb-bf45-a893a278b3c4">






