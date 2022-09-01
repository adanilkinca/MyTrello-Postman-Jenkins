# study

Running Newman with Docker commands
===================================


Running a remote collection (hello world example)
-------------------------------------------------

docker run -t postman/newman_ubuntu1404 run "https://www.getpostman.com/collections/8a0c9bc08f062d12dcda"

Temporary workaround in case the example above fails:

docker pull postman/newman_ubuntu1404:3.8.3

docker run -t postman/newman_ubuntu1404:3.8.3 --url="https://www.getpostman.com/collections/8a0c9bc08f062d12dcda"​


Running a local collection with environment
-------------------------------------------

docker run -v ~/collections:/etc/newman -t postman/newman_ubuntu1404 run "Trello.postman_collection.json" --environment="Trello API.postman_environment.json"
