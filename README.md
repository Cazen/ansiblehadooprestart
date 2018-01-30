# ansiblehadooprestart

Start & Stop Hadoop JVM With Ansible script
==============================================
:author: cazen.lee

Start and stop JVM with ansible script.

IBK has two type of hadoop cluster. It called collect cluster and analysis cluster

And each cluster has two types of group

- YARN related Server : hadoop-rm, hadoop-mrhistory, hadoop-ats, hadoop-worker...
- HDFS related Server : hadoop-zkfc, hadoop-nn, hadoop-jn...

ex. collect-hadoop-zkfc, collect-hadoop-ats...

### Usage
###### This usage based on IBK specific environment but surely can be extended with well-formed hosts file

Just call

    $ ansible-playbook restart-all.yml

The script will stop the JVMs, wait for 30 seconds, and restart them all.