Do as instructed in http://debian.neo4j.org/. It requires Java 8, so make sure that it has been already installed in your system.

wget -O - https://debian.neo4j.org/neotechnology.gpg.key | sudo apt-key add -
echo 'deb http://debian.neo4j.org/repo stable/' >/tmp/neo4j.list
sudo mv /tmp/neo4j.list /etc/apt/sources.list.d
sudo apt-get update

Install neo4j. Here, I use neo4j community edition.

apt-get install neo4j

Then, start neo4j

service neo4j start

Open the GUI

http://localhost:7474

<insert screenshot>

The default login/password is neo4j/neo4j. It requires the user to change the password for the first-time access.


*Cypher*

Cypher is the declarative query language used for data manipulation in Neo4j. It is similar to SQL.

You can use the GUI prompt to execute Cypher. For example, the following will create something.

CREATE(n:Business{ name: 'GraphStory', description: 'Graph as a service'})
