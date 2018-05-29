# log-stash

Install Logstash on Cent OS 7

VM on GCP

Logstash requires Java 8, an open-source distribution such as [OpenJDK.](https://www.server-world.info/en/note?os=CentOS_7&p=jdk8&f=2)

```
sudo yum -y install java-1.8.0-openjdk java-1.8.0-openjdk-devel
```

```
java -version
```

```
sudo yum -y install wget
```

Download Logstash 6.2.4 rpm

```
wget https://artifacts.elastic.co/downloads/logstash/logstash-6.2.4.rpm
sudo rpm -ivh logstash-6.2.4.rpm
```
Create a simple configuration file:
```
vim hello-world-logstash.conf
```

```
input {
        stdin { }
}
output {
        stdout{}
}
```

```
whereis logstash
```

Run configuration file:

```
sudo /usr/share/logstash/bin/logstash -f ~/hello-world-logstash.conf
```
