# Projects

Up Hadoop Cluster   : <start-all.sh> 
Down Hadoop Cluster : <stop-all.sh>
Check what services are up: <jps>
Check NameNode webUI port listening : <sudo netstat -tuln | grep 50070>

NameNode WebUI - http://localhost:50070/dfshealth.html#tab-overview
All Cluster Application UI- http://localhost:8088/cluster

#-------------------------------------------------------------------------------------------------------------------#
#Hadoop config files location: /usr/local/hadoop/etc/hadoop
#core-site.xml
<configuration>
        <property>
        <name>fs.defaultFS</name>
        <value>hdfs://localhost:9000</value>
        </property>
</configuration>    

#hdfs-site.xml
<configuration>
    <property>
	<name>dfs.replication</name>
	<value>1</value>
    </property>
    <property>
        <name>dfs.name.dir</name>
        <value>/home/phoenix/hadoop/dfs</value> # Need a persistent directory to store runtime config data 
    </property>
    <property>
    	<name>dfs.namenode.http-address</name>
 	<value>localhost:50070</value>
    </property>

</configuration>
#-------------------------------------------------------------------------------------------------------------------#
#logs directory: /usr/local/hadoop/logs


