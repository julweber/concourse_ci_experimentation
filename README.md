# Concourse experiments
This serves as a starting point for using concourse ci.

## Installation
Concourse CI can be installed on kubernetes using docker-compose:

```
docker-compose up -d
```

Afterwards ensure to install the fly executable for your according system into your path.

## Login
```
fly -t tutorial login -c http://localhost:8080
# user: test ; pw: test
fly -t tutorial status
```

## Execute pipeline/task
```
cd pipelines
fly -t tutorial e -c task_hello_world.yml
```

## Set pipeline
```
fly -t tutorial sp -c basic_pipeline.yml -p hello-world-pipeline
```