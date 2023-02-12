
This project is about building a web Application :- The AirBnB_clone console

The console or command interpreter allows you to to create, update, destroy, store and persist objects to a JSON file.


HOW TO START AND USE THE COMMAND INTERPRETER

Move in to the directory
$ cd AirBnB_clone

Execute the console file
/AirBnB_clone$ ./console.py


THE CONSOLE COMMANDS USED
*create   - Creates a new instance of the class passed by argument

show      - Prints the string representation of an instance.

*destroy  - Deletes an instance that was already created

all       - Prints string representation of all instances or of all instances of a specified class

*update   - Updates an instance attribute if exists otherwise create it

help      - Show all commands or display information about a specific command

quit      - Exit the console

EOF       - Exit the console. 


HOW THE COMMANDS ARE USED 
create    -> create <class_name>

show      -> show <class_name> <object_id> ; <class_name>.show(<object_id>)()

destroy   -> destroy <class_name> <object_id ; <class_name>.destroy(<object_id>)()

all       -> all <class_name> ; <class_name>.all()
update    -> update <class_name> <object_id> <attribute name> “<attribute value>” ; <class name>.update(<object_id>, <attribute name>, <attribute value>) ; <class name>.update(<object_id>, <dictionary representation>)

help      -> help ; help <command_name>

quit      -> quit

EOF    



COMMANDS USAGE:-
create    -> create <class_name>

show      -> show <class_name> <object_id> ; <class_name>.show(<object_id>)()

destroy   -> destroy <class_name> <object_id ; <class_name>.destroy(<object_id>)()

all       -> all <class_name> ; <class_name>.all()

update    -> update <class_name> <object_id> <attribute name> “<attribute value>” ; <class name>.update(<object_id>, <attribute name>, <attribute value>) ; <class name>.update(<object_id>, <dictionary representation>)

help      -> help ; help <command_name>

quit      -> quit

EOF       -> EOF ; (ctrl + d)






INTERACTIVE MODE TESTING
Example 1: Using create, count and all commands
:~/H/AirBnB_clone$ ./console.py 
(hbnb) all
[]
(hbnb) create Place
492f60f3-ff1e-43c7-bb11-f8407b04dd59
(hbnb) create BaseModel
99f01e9a-99c0-42af-8c10-c35cadee1d8f
(hbnb) BaseModel.count()
1
(hbnb) all
["[Place] (492f60f3-ff1e-43c7-bb11-f8407b04dd59) {'id': '492f60f3-ff1e-43c7-bb11-f8407b04dd59', 'created_at': datetime.datetime(2020, 7, 1, 11, 36, 24, 576486), 'updated_at': datetime.datetime(2020, 7, 1, 11, 36, 24, 576530)}", "[BaseModel] (99f01e9a-99c0-42af-8c10-c35cadee1d8f) {'id': '99f01e9a-99c0-42af-8c10-c35cadee1d8f', 'created_at': datetime.datetime(2020, 7, 1, 11, 36, 30, 773211), 'updated_at': datetime.datetime(2020, 7, 1, 11, 36, 30, 773236)}"]
(hbnb)


Example 2: Using basic update with an Id and show command
(hbnb) update BaseModel 99f01e9a-99c0-42af-8c10-c35cadee1d8f first_name "Airbnb"
(hbnb) show BaseModel 99f01e9a-99c0-42af-8c10-c35cadee1d8f
[BaseModel] (99f01e9a-99c0-42af-8c10-c35cadee1d8f) {'id': '99f01e9a-99c0-42af-8c10-c35cadee1d8f', 'created_at': datetime.datetime(2020, 7, 1, 11, 36, 30, 773211), 'updated_at': datetime.datetime(2020, 7, 1, 11, 36, 30, 773236), 'first_name': 'Console'}
(hbnb) Place.update("492f60f3-ff1e-43c7-bb11-f8407b04dd59", "first_name", "Airbnb")
(hbnb) show Place 492f60f3-ff1e-43c7-bb11-f8407b04dd59
[Place] (492f60f3-ff1e-43c7-bb11-f8407b04dd59) {'id': '492f60f3-ff1e-43c7-bb11-f8407b04dd59', 'created_at': datetime.datetime(2020, 7, 1, 11, 36, 24, 576486), 'updated_at': datetime.datetime(2020, 7, 1, 11, 36, 24, 576530), 'first_name': 'Console'}


Example 3: Using update with a dictionary
(hbnb) BaseModel.update("99f01e9a-99c0-42af-8c10-c35cadee1d8f", {'first_name': "Petter", "age": 45})
(hbnb) show BaseModel 99f01e9a-99c0-42af-8c10-c35cadee1d8f
[BaseModel] (99f01e9a-99c0-42af-8c10-c35cadee1d8f) {'id': '99f01e9a-99c0-42af-8c10-c35cadee1d8f', 'created_at': datetime.datetime(2020, 7, 1, 11, 36, 30, 773211), 'updated_at': datetime.datetime(2020, 7, 1, 11, 36, 30, 773236), 'first_name': 'Petter', 'age': '45'}


Example 4: Using destroy and count command
(hbnb) BaseModel.destroy("99f01e9a-99c0-42af-8c10-c35cadee1d8f")
(hbnb) all


PYTHON SCRIPTS
Allowed editors: vi, vim, emacs

All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)

All your files should end with a new line

The first line of all your files should be exactly #!/usr/bin/python3

A README.md file, at the root of the folder of the project, is mandatory
