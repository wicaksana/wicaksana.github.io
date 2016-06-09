---
layout: post
title:  "How to Backup Neo4j Community"
date:   2016-04-22 21:21:45 +0200
categories: Neo4j
-----------------

There is no online backup feature for Neo4j Community. I believe there are two ways to backup:
1. Use neo4j-shell dump
    neo4j-shell -c dump > dump.cypher
    Then restore in another server:
    neo4j-shell -file dump.cypher
    
2. Copy the whole content of graph.db and put it on another Neo4j server
    Make sure to shutdown Neo4j first to prevent data inconsistencies
    Do the following:
    - cd /var/lib/neo4j/data/databases
    - tar -zcvf graph.db.tar.gz graph.db
    - (move the resulted compressed file onto the backup server)
    At the backup server, do the following:
    - service neo4j stop
    - cd /var/lib/neo4j/data/databases
    - rm -rf graph.db
    - tar -xzvf graph.db.tar.gz
    (verify that the ownership and file permission of the unpacked files match with the original ones at backup server)
    - service neo4j start
    (verify that everything's going right. See Neo4j log: /var/log/neo4j/neo4j/log)
