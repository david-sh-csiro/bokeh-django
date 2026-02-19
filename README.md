# bokeh-django
Minimal reproduction for a reproducing web socket subprotocols

# Dev environment
## Create venv
python -m venv venv

source venv/bin/activate
## Install Packages
pip install -r requirements.txt


# Run
`cd django_embed`

Granian `granian --host 127.0.0.1 --port 8000 --access-log django_embed.asgi:application --interface asgi`

Daphne `daphne --bind 127.0.0.1 --port 8000 --access-log - django_embed.asgi:application`

Uvicorn `python -m uvicorn --host 127.0.0.1 --port 8000 django_embed.asgi:application`

# Issue reproduction

Load up the app and click the top link.
Or go directly to http://localhost:8000/sea_surface

In the logs You should be able to see a print out of self.scope['subprotocols']
