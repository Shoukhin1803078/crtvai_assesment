# Flask Chatbot with MySQL Integration

A Flask-based chatbot application featuring session management, persistent storage, and a web interface.

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

### Conversation States
1. INITIAL → Awaiting "hello"
2. WAITING_FOR_NAME → Collecting user name
3. WAITING_FOR_SONG → Getting favorite song
4. COMPLETED → Conversation finished

## 🚀 Installation

### Prerequisites
- Python 3.8+
- MySQL Server
- pip (Python package manager)

### Step 1: Clone Repository
```bash
git clone <repository-url>
cd flask-chatbot
```

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

3. **Access Chatbot**
- Open web browser
- Navigate to `http://localhost:5000`
- Enter phone number to begin chat

## 💬 Usage Examples

### Starting Conversation
```
User: hello
Bot: What is your name?
```

### Complete Flow
```
User: hello
Bot: What is your name?
User: John
Bot: Hello John, what is your favorite song?
User: Bohemian Rhapsody
Bot: Playing Bohemian Rhapsody
```

## 🔧 Troubleshooting

### Common Issues:

1. **Database Connection Failed**
   - Verify MySQL is running
   - Check credentials in db_config
   - Ensure database exists

2. **Application Won't Start**
   - Check if port 5000 is available
   - Verify all dependencies are installed
   - Ensure Python version compatibility

## 🔒 Security Features

- SQL injection prevention
- Input validation
- Session isolation
- Secure data handling

## 🤝 Contributing

1. Fork repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Submit pull request

## 📝 License

MIT License - see LICENSE file for details.

---
Developed for Technical Assessment | 2024
