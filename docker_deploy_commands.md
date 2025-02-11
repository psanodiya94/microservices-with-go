# Docker Swarm Deployment Commands

## Initializing Swarm

### **docker swarm init**
- **Description**: Initialize a swarm.
- **Usage**: `docker swarm init [OPTIONS]`
- **Example**: 
  - `docker swarm init` (on the manager node)
  - `docker swarm init --advertise-addr ` (if specifying an advertise address)

## Managing Swarm Nodes

### **docker node ls**
- **Description**: List nodes in the swarm.
- **Usage**: `docker node ls [OPTIONS]`
- **Example**: `docker node ls`

### **docker node update**
- **Description**: Update a node in the swarm.
- **Usage**: `docker node update [OPTIONS] NODE ID`
- **Example**: `docker node update --label-add foo=bar `

### **docker node rm**
- **Description**: Remove one or more nodes from the swarm.
- **Usage**: `docker node rm NODE [NODE...]`
- **Example**: `docker node rm `

## Managing Services

### **docker service create**
- **Description**: Create a new service.
- **Usage**: `docker service create [OPTIONS] IMAGE [COMMAND] [ARG...]`
- **Example**: 
  - `docker service create --name myweb --replicas 3 nginx`

### **docker service ls**
- **Description**: List services.
- **Usage**: `docker service ls [OPTIONS]`
- **Example**: `docker service ls`

### **docker service ps**
- **Description**: List the tasks of one or more services.
- **Usage**: `docker service ps [OPTIONS] SERVICE [SERVICE...]`
- **Example**: `docker service ps myweb`

### **docker service update**
- **Description**: Update a service.
- **Usage**: `docker service update [OPTIONS] SERVICE`
- **Example**: `docker service update --replicas=5 myweb`

### **docker service rm**
- **Description**: Remove one or more services.
- **Usage**: `docker service rm SERVICE [SERVICE...]`
- **Example**: `docker service rm myweb`

## Scaling Services

### **docker service scale**
- **Description**: Scale one or multiple replicated services.
- **Usage**: `docker service scale SERVICE=REPLICAS [SERVICE=REPLICAS...]`
- **Example**: `docker service scale myweb=5`

## Managing Stacks

### **docker stack deploy**
- **Description**: Deploy new stack or update an existing stack.
- **Usage**: `docker stack deploy [OPTIONS] STACK`
- **Example**: `docker stack deploy -c docker-compose.yml myapp`

### **docker stack ls**
- **Description**: List stacks.
- **Usage**: `docker stack ls [OPTIONS]`
- **Example**: `docker stack ls`

### **docker stack services**
- **Description**: List the services in the stack.
- **Usage**: `docker stack services STACK`
- **Example**: `docker stack services myapp`

### **docker stack rm**
- **Description**: Remove one or more stacks.
- **Usage**: `docker stack rm STACK [STACK...]`
- **Example**: `docker stack rm myapp`

### **docker swarm leave**
- **Description**: Node left the swarm.
- **Usage**: `docker swarm leave --force`
- **Example**: `docker swarm leave --force`

## Managing Secrets

### **docker secret create**
- **Description**: Create a secret from a file or STDIN as content.
- **Usage**: `docker secret create [OPTIONS] SECRET file|-`
- **Example**: `docker secret create my_secret ./secret.txt`

### **docker secret ls**
- **Description**: List secrets.
- **Usage**: `docker secret ls [OPTIONS]`
- **Example**: `docker secret ls`

---

These commands provide the basics for managing and deploying services in a Docker Swarm environment. Always refer to the Docker documentation for the most up-to-date and comprehensive information on each command.
