
# SynthMind 🤖

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.x-FF4B4B.svg)](https://streamlit.io/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Cross--Platform-lightgrey.svg)](https://github.com/SaYaN00101/SynthMind)
[![Build Status](https://img.shields.io/badge/Build-Passing-success.svg)](https://github.com/SaYaN00101/SynthMind)

![Project Banner](https://github.com/user-attachments/assets/9e5eecf7-c80d-4b8a-8b16-70ddb538379a)

## 🎯 Overview

SynthMind is a sophisticated AI chatbot platform that combines the power of local large language models with robust user management and secure data persistence. Built using Streamlit and powered by Ollama's Gemma-2B model, it offers a professional-grade solution for organizations and individuals who need reliable, private, and efficient AI conversations.

With its focus on privacy and local processing, SynthMind eliminates the need for external API calls while maintaining high performance and real-time responses. The integration of MySQL ensures that all user data and conversations are securely stored and easily accessible.

Perfect for businesses, developers, and privacy-conscious users, SynthMind demonstrates how modern AI can be implemented with both power and responsibility.


 ## ✨ Features

### Core Functionality
🔐 **Advanced Authentication**
- Secure user registration with profile management
- Protected login system
- Session-based authentication

🤖 **AI Integration**
- Real-time chat with Gemma-2B model
- Local processing for enhanced privacy
- Fast response times with no API latency

💾 **Data Management**
- MySQL-based persistent storage
- Session-wise chat history
- Automatic conversation backup

### User Experience
🎨 **Interface**
- Clean, modern Streamlit UI
- Responsive design
- Intuitive navigation

🔄 **Session Management**
- Multiple chat sessions
- Easy history browsing
- Session titling and organization

🔒 **Privacy & Security**
- No external API dependencies
- Local LLM processing
- Secure data storage


## 🛠️ Tech Stack

### Core Technologies
- **Python 3.9+**: Primary development language
- **Streamlit**: Frontend framework for web interface
- **MySQL**: Robust data persistence and user management
- **Ollama**: Local LLM integration platform

### AI Model
- **Gemma-2B**: High-performance language model

### Additional Libraries
- **UUID**: Unique session identification
- **datetime**: Timestamp management
- **logging**: System monitoring and debugging
- **mysql-connector-python**: Database connectivity


## � Installation

### Prerequisites
- Python 3.9 or higher
- MySQL Server (XAMPP/WAMP/Standalone)
- [Ollama](https://ollama.com) for LLM support

### Step-by-Step Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/SaYaN00101/SynthMind.git
   cd SynthMind
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Database Setup**
   ```sql
   CREATE DATABASE synthmind_AI_DB;
   USE synthmind_AI_DB;

   CREATE TABLE user_data (
       ID INT AUTO_INCREMENT PRIMARY KEY,
       Name VARCHAR(250),
       Age INT,
       Gender VARCHAR(30),
       Country VARCHAR(150),
       City VARCHAR(250),
       UserID VARCHAR(100) UNIQUE,
       password VARCHAR(100),
       RegisteredAt DATETIME
   );

   CREATE TABLE chat_history (
       ID INT AUTO_INCREMENT PRIMARY KEY,
       UserID VARCHAR(100),
       messege_role ENUM('user', 'assistant'),
       message_content LONGTEXT,
       DateTime DATETIME DEFAULT CURRENT_TIMESTAMP(),
       Session_ID VARCHAR(100),
       Session_Title VARCHAR(250)
   );
   ```

4. **Configure Environment**
   Create `.streamlit/secrets.toml`:
   ```toml
   [mysql]
   host = "localhost"
   user = "your_mysql_username"
   password = "your_mysql_password"
   database = "synthmind_AI_DB"
   port = 3306
   ```

5. **Set Up AI Model**
   ```bash
   ollama pull gemma:2b
   ```

6. **Launch Application**
   ```bash
   streamlit run app.py
   ```

   Access the application at `http://localhost:8501`


## 📸 Screenshots

![Login Interface](https://github.com/user-attachments/assets/1cc07601-54a8-4b01-b9b5-ae4f6d99268c)
*Secure login interface with user authentication*

![Chat Dashboard](https://github.com/user-attachments/assets/e8217d3d-6213-4436-b5f0-8ce101692983)
*Main chat interface with session management*

## 🗺️ Roadmap

### Short-term Goals
- [ ] Voice input/output capabilities
- [ ] Multi-language support
- [ ] Emotion detection in responses
- [ ] Enhanced error handling

### Mid-term Goals
- [ ] Admin dashboard for user management
- [ ] Advanced analytics and usage metrics
- [ ] API integration options
- [ ] Custom model fine-tuning

### Long-term Vision
- [ ] Cloud deployment infrastructure
- [ ] Enterprise-grade security features
- [ ] Mobile application development
- [ ] AI model marketplace integration



 ## 👥 Contributing

We welcome contributions to SynthMind! Here's how you can help:

1. **Fork** the repository
2. Create a **feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. Submit a **Pull Request**

For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🌟 Acknowledgments

Special thanks to:
- [Streamlit](https://streamlit.io/) for the incredible UI framework
- [Ollama](https://ollama.com/) for local LLM capabilities
- The Python and MySQL communities for their invaluable tools
- All contributors who help make SynthMind better

## 👤 Contact

Sayan - [@SaYaN00101](https://github.com/SaYaN00101)

Project Link: [https://github.com/SaYaN00101/SynthMind](https://github.com/SaYaN00101/SynthMind)

---

<div align="center">
Made with ❤️ by the SynthMind Team
</div>
