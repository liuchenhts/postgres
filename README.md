# postgres server run by docker compose

Docker compose for postgres database server

1. ./start-server, to start a container as the postgres server service.
2. ./stop-server, to stop and remove service related resources.

## postgres server env vars in the container

### best practise is to inject env vars from exteral config into the container

1. best practise is to use external env file or apis to injest env vars to container from dev to prod
2. k8s inject env vars from helm chart values, some may further retrieve from vault to inject
3. env_file in docker-compose.yml can point to any file path other than .evn
4. .env defines all env vars needed for postgres server container. eg. the super uer password

### other options to inject env vars into the container

1. use environment: to define the env vars needs to be injected into the container
2. use - env_in_container: $env_in_local under the environment: to define
3. env_in_container is the env var will be injected into container
4. env_in_local is the env var either defined in .env file or in local system env
