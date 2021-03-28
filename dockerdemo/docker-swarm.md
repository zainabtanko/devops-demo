# Initialise Docker Swarm
`docker swarm init --advertise-addr <IP Address>`

# List Nodes
`docker node ls`

# Create Service
`docker service create –name Apache2 –mode global -d -p 8003:80 httpd`

# List services
`Docker service ls`

# scale services
`docker service scale Apache2=5`

# Check docker containers in a service
`docker service ps mysql`
