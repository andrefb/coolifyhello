# Django Hello World + PostgreSQL

Projeto básico Django com PostgreSQL para deploy no Coolify.

## Rodando localmente

1. Clone o repositório
2. Crie um ambiente virtual: `python -m venv venv`
3. Ative: `source venv/bin/activate`
4. Instale dependências: `pip install -r requirements.txt`
5. Crie arquivo `.env` baseado no `.env.example`
6. Rode migrações: `python manage.py migrate`
7. Inicie servidor: `python manage.py runserver`

## Deploy no Coolify

- Build Pack: Nixpacks
- Start Command: `python manage.py migrate && python manage.py collectstatic --noinput && gunicorn mysite.wsgi:application --bind 0.0.0.0:3000`
- Portas: 3000
- Variáveis de ambiente: DATABASE_URL, SECRET_KEY, DEBUG=False, ALLOWED_HOSTS
