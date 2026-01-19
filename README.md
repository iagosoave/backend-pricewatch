# PriceWatch Backend

API de monitoramento de preços.

## Rodar local

```bash
# Windows
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Linux/Mac
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Endpoints

- GET /api/products/ - Lista produtos
- POST /api/products/ - Cria produto
- GET /api/products/{id}/ - Detalhe
- DELETE /api/products/{id}/ - Remove
- POST /api/products/{id}/scrape/ - Atualiza preço
- GET /api/products/{id}/history/ - Histórico

## Deploy no Railway

1. Conecta o repo no Railway
2. Adiciona variáveis: SECRET_KEY, DEBUG=False, ALLOWED_HOSTS, CORS_ALLOWED_ORIGINS
