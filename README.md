# DESAFIO ITV

## Passos para executar a interface web: 

### 1 - Com o terminal aberto dentro do diretório da interface web, digitar:
python -m http.server (Por padrão, a porta utilizada será a 8000)

### 2 - Iniciar a simulação no terminal digitando:
export TURTLEBOT3_MODEL=waffle_pi
roslaunch turtlebot3_gazebo turtlebot3_autorace_2020.launch

### 3 - Iniciar web_video_server em outro terminal, digitando: 
rosrun web_video_server web_video_server _port:=11315

### 4 - Iniciar o rosbridge, o qual vai fazer a conexão entre a simulação e a interface web. Digitar no terminal: 
roslaunch rosbridge_server rosbridge_websocket.launch

### 5 - Tudo pronto. Agora é só abrir https://localhost/8000 (ou a porta que desejar configurar)

# Links úteis para instalação dos pacotes necessários:

Instalação do ROS: http://wiki.ros.org/Installation/Ubuntu
Instalação do web_video_server: http://wiki.ros.org/web_video_server

### Obs 1: O Roslibjs está sendo importado no código utilizando CDN.
### Obs 2: Frameworks utilizados: VueJS (Javascript) e Bootstrap 4(CSS)


