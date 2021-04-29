# Docker : OK
'''
mkdir .config
sudo docker run -d --name code-server -p 8180:8080 \
  -v "$PWD/.config:/home/coder/.config" \
  -v "$HOME/repos:/workspace" \
  -u "$(id -u):$(id -g)" \
  -e "DOCKER_USER=$USER" \
  codercom/code-server:latest \ 
 '''

# Docker compose : OK
sudo docker-compose --project-name vscode --project-directory $(pwd) up -d


