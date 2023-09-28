# django_webhosting
# hosted on: https://www.pythonanywhere.com/

# On Bash
git clone https://github.com/Abhishek-2502/django_webhosting
mkvirtualenv venv
cd django_webhosting
cd django_webhosting
pip install django

1>In Settings.py:
  Debug = true
  ALLOWED_HOSTS = ['AbhishekRajput.pythonanywhere.com']
  'DIRS': ['/home/AbhishekRajput/django_webhosting/django_webhosting/templates'],

2> IN Code Section:
In WSGI configuration file:

# +++++++++++ DJANGO +++++++++++
# To use your own django app use code like this:
import os
import sys
#
## assuming your django settings file is at '/home/AbhishekRajput/mysite/mysite/settings.py'
## and your manage.py is is at '/home/AbhishekRajput/mysite/manage.py'
path = '/home/AbhishekRajput/django_webhosting/django_webhosting'                             #
if path not in sys.path:
    sys.path.append(path)
#
os.environ['DJANGO_SETTINGS_MODULE'] = 'django_webhosting.settings'                           #
#
## then:
from django.core.wsgi import get_wsgi_application
application = get_wsgi_application()

3> IN Virtualenv Section:
   add 'venv'
