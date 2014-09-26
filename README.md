# Introduction
## This is a Apache Mesos cluster that runs Apache Karaf, Chronos, Marathon, and a loads a blueprint file with a simple transfer to MQ.
==============================
I need to set marathon and chronos to start automatically. 
- For now, just start the processes manually
- sudo nohup /opt/chronos/bin/start-chronos.bash --master zk://localhost:2181/mesos --zk_hosts zk://localhost:2181/mesos --http_port 8081 > /var/log/chronos/nohup.log 2> /var/log/chronos/nohup.log < /dev/null &
- nohup /opt/marathon-0.7.0/bin/start --master zk://localhost:2181/mesos --zk_hosts localhost:2181 > /var/log/marathon/nohup.log 2> /var/log/marathon/nohup.log < /dev/null & 
