# mysql-cdc-projects
A listing of projects to get data streams out of MySQL

List of projects that will let you do replication from MySQL to Kafka.

Project name                 | Site                                                   | Description
-----------------------------|--------------------------------------------------------|-------------
sqlstream                    | https://github.com/pyr/sqlstream                       | Directly maps MySQL events to JSON, with no interpretation. Written in Java. Replicates to Kafka.
databus                      |  https://github.com/linkedin/databus                   | Precursor to Kafka. Reads from MySQL and Oracle, and replicates to its own log structure. In production use at LinkedIn. No Kafka integration. Uses Open Replicator.
aesop                        | https://github.com/Flipkart/aesop                      | Built on top of Databus. In production use at http://www.flipkart.com/. Allows you to plug in your own code to transform/process the MySQL events.
mypipe                       | https://github.com/mardambey/mypipe                    | Reads MySQL event stream, and emits events corresponding to INSERTs, DELETEs, UPDATEs. Written in Scala. Emits Avro to Kafka.
Tungsten Replicator          |  https://code.google.com/p/tungsten-replicator         | Reads from MySQL and replicates to its own log structure. Allows plugging in your own code to process the events however you want. Open source component of [Continuent](http://www.continuent.com/solutions), a commercial company that does database replication.
Open Replicator              | https://code.google.com/p/open-replicator/             | Library that parses MySQL binary logs and calls your code to process them. Does not seem to be maintained.
mysql-binlog-connector-java  |  https://github.com/shyiko/mysql-binlog-connector-java | Library that parses MySQL binary logs and calls your code to process them. Fork/rewrite of Open Replicator. Has tests.

