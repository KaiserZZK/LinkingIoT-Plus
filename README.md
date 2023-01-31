# Linking IoT (Spring 22)

This project is to represent IoT objects in graph-based database, analyze the linkages between devices, and alert users when potential there is a potential conflit in a command before it is being excuted. 


## To Bootstrap the Project
### Install Neo4j database
Download neo4j desktop: https://neo4j.com/download/

Once you have downloaded these, open the neo4j desktop app and click on new project. This will create a new project and this will be your project hosting your database. You can then create a database (and start the database) from the menu which will then start a database listening on http://localhost:7474/browser/

Go to the http://localhost:7474/browser/ and type in your credentials which you have setup when you are creating the database (username is neo4j by default). This will give you the CLI to the neo4j graph.


Once the above is setup, go to `app/template/links.html` and change the user name and password to what you have setup in the above. 

      server_url: "bolt://localhost:7687",
      server_user: "xxxxxxx",
      server_password: "xxxxxxx",

You might want to change the password and user in `app/neo4j_service.py`, `app/models.py` and `config/config.ini`.

### Install dependencies and run Flask app
Once the above is done, you can create a virtual environment (e.g., python3 venv or similar) to install dependencies and run the flask app.
Install dependencies by running `pip install -r requirements.txt` under app directory. 
Start the app by running `python3 app.py`

For registration of thing. Open `http://localhost:5000/`. Use the home setup directory under linked_features. Remember that you need to register the dependency first before the actual node. 

The order of registration:

- zone.json
- kitchen.json
- livingroom.json
- wifi.json
- tab.json
- smarthomecontroller
- cam
- lightsystem
- plug1, plug2
- light1, light2
