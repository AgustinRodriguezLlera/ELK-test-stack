# ELK Test 

This compose file creates a Stack with ElasticSearch and Kibana, both in a container each one, for quick testing.

Not a full ELK stack really (there's no Logstash).

This start a container with ElasticSearch, and a container with Kibana, configured to see logs in ES.

Elasticsearch shares port 9200 and 9300, and kibana shares port 5601 for viewing the logs.

**THIS STACK IS JUST FOR TESTING AND DEVELOPING PURPOSES!!!!!**
 
## Pre-Requistes
Just have *docker* and *docker-compose* installed. Don't  care the OS (Windows, Linux, OS X, whatever), it's a very basic stack, for quick testing.


## Running

Clone this repo, and just run `docker-compose up` inside the repo's folder:
 
```
git clone https://github.com/ggMartinez/ELK-test-stack.git
cd ELK-test-stack
docker-compose up
```

As you can see in the compose file, there's no peristency, so everything is ephemeral, unless you want to modify things. I will not cover that, this stack is for quick tests only, and I made it like that for the developers on my job so they can test locally instead of breaking our ELK prod stack :)

## Data persistency
As the main paragraph says: **THIS STACK IS JUST FOR TESTING AND DEVELOPING PURPOSES!!!!!**

This stack is just for saving quick data into ElasticSearch, from a service, app, or whatever. It has no persistence configured, so if you destroy the stack, all data will be lost.

