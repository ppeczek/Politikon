web: newrelic-admin run-program python manage.py run_gunicorn -b "0.0.0.0:$PORT" -w 2 --preload  --log-level=debug
worker: python manage.py celery beat --loglevel=INFO & newrelic-admin run-program python manage.py celery worker --loglevel=DEBUG --concurrency=1
