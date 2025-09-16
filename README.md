# Warbler

Warbler is a Twitter-inspired microblogging web application built with Flask. Users can create accounts, post short messages (“warbles”), follow other users, like messages, and view personalized feeds. This project demonstrates full-stack development with authentication, relational databases, and responsive front-end design.

**Live Demo:** https://warbler-3im0.onrender.com 

---

## Features

- User registration, login, and secure authentication with Flask-Bcrypt  
- Create, edit, and delete messages (“warbles”)  
- Follow/unfollow other users and view follower/following lists  
- Like/unlike messages and view liked messages  
- Responsive front-end using HTML, CSS, Jinja2 templates, and Bootstrap  

---

## Technologies

- **Backend:** Python, Flask, Flask-Bcrypt, Flask-SQLAlchemy  
- **Frontend:** HTML, CSS, Bootstrap, Jinja2 templates  
- **Database:** PostgreSQL  
- **Authentication & Sessions:** Flask  
- **Testing:** Flask-Testing / unittest  

---

## Installation

1. Clone the repo:  
  ```bash
  git clone https://github.com/yourusername/warbler.git
  cd warbler
  ```
2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Mac/Linux
   venv\Scripts\activate  # Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set environment variables:
   ```bash
   export FLASK_APP=app.py
  export FLASK_ENV=development
  export DATABASE_URL=postgresql:///warbler
  ```
5. Initialize the database:
  ```bash
  flask db init
  flask db migrate
  flask db upgrade
  ```
6. Run the app:
   ```bash
   flask run
   ```

Visit `http://127.0.0.1:5000` to start using Warbler.

---

## Database Models

- **User**: `id`, `username` (unique), `email`, `password`
- **Message**: `id`, `text`, `timestamp`, `user_id`
- **Follows**: `user_following_id`, `user_being_followed_id`
- **Likes**: `id`, `user_id`, `message_id`

## License
MIT License
