# bokeh-django
Minimal reproduction for a reproducing web socket subprotocols

# Dev environment
## Create venv
python -m venv venv
source venv/bin/activate
## Install Packages
pip install -rd requirements.txt


# Run
Granian `granian --host 127.0.0.1 --port 8000 --access-log django_embed.asgi:application --interface asgi`

Daphne `daphne --bind 127.0.0.1 --port 8002 --access-log - django_embed.asgi:application`