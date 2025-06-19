# python-blog-system
git clone https://github.com/yourusername/python-blog-system.git
cd python-blog-system
# Windows
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
FLASK_APP=run.py
FLASK_ENV=development
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///app.db
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
flask shell
>>> from app.models import User
>>> admin = User(username='admin', email='admin@example.com', is_admin=True)
>>> admin.set_password('adminpassword')
>>> db.session.add(admin)
>>> db.session.commit()
>>> exit()
>>> flask run
