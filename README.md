# Cloud Screw App

"Cloud Screw App" is a small flask web application designed to accept JSON data from the Ruuvi Gateway and display it on a dashboard.

- Accepts JSON data from Ruuvi Gateway (currently only accepts decoded data)
- Flask framework, Gunicorn WSGI
- SocketIO for real-time data
- Bootstrap for the dashboard layout

## 
### To run (locally):
First install required modules:
```
pip install -r requirements.txt 
```
Then run with gunicorn:
```
gunicorn --worker-class geventwebsocket.gunicorn.workers.GeventWebSocketWorker --workers 1 --bind localhost:[PORT] app.app:app
```
- Replace [PORT] with port of your choosing


