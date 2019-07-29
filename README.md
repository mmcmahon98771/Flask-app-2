# Flask-app-2
import requests

api_url = 'https://www.quandl.com/api/v1/datasets/WIKI/%s.json' % BLS
session = requests.Session()
session.mount('http://', requests.adapters.HTTPAdapter(max_retries=3))
raw_data = session.get(api_url)
