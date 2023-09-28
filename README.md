# django_webhosting
# hosted on: https://www.pythonanywhere.com/

# 1.On Bash <br>
git clone https://github.com/Abhishek-2502/django_webhosting <br>
mkvirtualenv venv <br>
cd django_webhosting <br>
cd django_webhosting <br>
pip install django <br>

# 2. Other <br>
1>In Settings.py: <br>
  Debug = true <br>
  ALLOWED_HOSTS = ['AbhishekRajput.pythonanywhere.com'] <br>
  'DIRS': ['/home/AbhishekRajput/django_webhosting/django_webhosting/templates'], <br>

2> IN Code Section: <br>
In WSGI configuration file: <br>

 +++++++++++ DJANGO +++++++++++ <br>
import os <br>
import sys <br>

path = '/home/AbhishekRajput/django_webhosting/django_webhosting' <br>                            #
if path not in sys.path: <br>
    sys.path.append(path) <br>

os.environ['DJANGO_SETTINGS_MODULE'] = 'django_webhosting.settings' <br>                          #

from django.core.wsgi import get_wsgi_application <br>
application = get_wsgi_application()

3> IN Virtualenv Section: <br>
   add 'venv'
