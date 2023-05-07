# CS361-A8
Microservice that retrieves National Park Image locations for an App using python sockets.
This microservice will depend on a local folder of downloaded National Park Images.

The app will request the image via Client.py and consequently Client.py will connect to Server.py
through sockets. If there is a valid national park image that corresponds with the input
from the app, it will return that location of the image to the client and consequently to the
user in the app.

Server.py
This server will listen on a socket for client connections. Upon successful connection, the server
will wait for client to send search query for National Park or "quit". Upon successful retrieval,
Server.py will return to Client.py location path of image that is stored locally. Otherwise an error message will be
returned to the Client.py. Server.py stays active listening to client connections until a client sends "quit".

Client.py
Client.py must be run every time an image request is made from the app. Client.py connects to image retrieval server
and waits for search query from app/user that is supposed to be the name of National Park. Search query is case sensitive.
Upon successful retrieval, Client.py will show location path of image that is stored locally. Otherwise an error message will be
returned to the Client.py. Client.py closes after each retrieval or error. Client.py can close the Server.py via "quit" command.

Start Here:
1. Install python and relevant packages on your IDE.
2. Download Server.py and Client.py
3. First run the Server.py in Terminal/powershell
4. Then run Client.py in the terminal/powershell
5. Follow instructions in Client

UML Sequence Diagram:<img width="378" alt="UML Diagram" src="https://user-images.githubusercontent.com/84735585/236694331-1d9157c7-08bd-4b1a-8cb6-7edbdf90e146.png">
