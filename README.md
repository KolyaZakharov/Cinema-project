
# Cinema API
- Api service for cinema management written on DRF

## Features:
- JWT authenticated
- Admin panel /admin/
- Documentation is located via /api/doc/swagger/
- Managing orders and tickets
- Media files on movie image (stored in docker )
- Creating movies with actors , genres 
- Filtering movies and movie sessions
- Docker app starts only when db is available ( custom command via management/commands )

## Installing using GitHub:
1. Install Postgres and create DB
2. Copy this repository, by using your terminal:
```git
git clone https://github.com/KolyaZakharov/Cinema-project.git
```
3. Change directory to main project folder. Use this command:
```git
cd Cinama-project
```
4. Install venv, and activate it by using following commands:
```git
python3 -m venv venv
```
to activate on Windows:
```git
venv\Scripts\activate
```
to activate on Linux:
```git
source venv/bin/activate
```
5. Install dependencies (requirements):
```git
pip install -r requirements.txt
```
6. Run migrations to initialize database. Use this command:
```git
python manage.py migrate
```
7. Open file ```.env-sample``` and change environment variables to yours. Also rename file extension to ```.env```
8. Run server and use!
```git
python manage.py runserver
```
## Run with Docker:
- Docker should be installed
```
- docker-compose build
- docker-compose up
```

## Getting access:
- Create user via /api/user/register/
- Get user token via /api/user/token/
- Authorize with it on /api/doc/swagger/ OR 
- Install ModHeader extention and create Request header with value ```Bearer <Your access tokekn>```

## Contributing

For major changes, please open an issue first to discuss what you would like to change.