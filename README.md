# HiveJDBCDao


Prerequisites:
	
	Install Java
	Install Hadoop
	Install Hive and Hook to HDFS
	   
Config 

	Go to hive-site.xml under
	$HIVE_HOME/conf folder 
	
	<?xml version="1.0"?>
	<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>
	<configuration>
	<property>
	<name>hive.metastore.warehouse.dir</name>
	<value>/user/hive/warehouse</value>
	</property>
	<property>
	<name>fs.default.name</name>
	<value>hdfs://localhost:54310/</value>
	</property>
	<property>
	<name>mapred.job.tracker</name>
	<value>localhost:54311</value>
	</property>
	</configuration>

This is simple Java class that allows use to connect to Hive
     
       Create a Table
       Query Data
       Load Data and so on
       
 Please download the "hive-jdbc-standalone" Jar from the following add to class path        

     http://central.maven.org/maven2/org/apache/hive/hive-jdbc/2.3.2/
     
 Compile and Run HiveQuery.java
 
 
 Open JDBC connectors as follows 
 
 		Connection con = DriverManager.getConnection(
				"jdbc:hive2://sandbox-hdp.hortonworks.com:2181/default;password=hive;serviceDiscoveryMode=zooKeeper;user=hive;zooKeeperNamespace=hiveserver2");

   
