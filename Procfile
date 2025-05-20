web: gunicorn --access-logfile=- --bind=0.0.0.0:$PORT --forwarded-allow-ips='*' mysite.wsgi:application
release: python manage.py migrate --noinput

