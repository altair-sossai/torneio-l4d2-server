# Torneio de Left 4 Dead 2

A comunidade de **Left 4 Dead 2** onde estou inserido se organizou para realizar um campeonato com o objetivo de fortalecer as amizades dentro e fora do jogo. O torneio utiliza a regra de pontos corridos para definir os vencedores, algo muito parecido com o que acontece nos campeonatos de futebol.

Para a realização dos jogos criamos um servidor utilizando Linux e fizemos diversas customizações para atender melhor a ideia do torneio.

## Organização

https://steamcommunity.com/profiles/76561198866194001/<br/>
https://steamcommunity.com/id/XxNero_94/<br/>
https://steamcommunity.com/id/altairsossai/<br/>

## Links da aplicação
A aplicação está disponível nos endereços abaixo:

Site do torneio:<br/>
https://torneio-l4d2.azurewebsites.net/

Front-end:<br/>
https://github.com/altair-sossai/torneio-l4d2-front-end

Back-end:<br/>
https://github.com/altair-sossai/torneio-l4d2-back-end

## Criar um novo servidor
```bash
cd /home
sudo mkdir steam
cd /home/steam

sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install screen -y
sudo apt-get install ufw -y
sudo apt-get install lib32gcc1 libc6-i386 -y
sudo apt-get install wget -y
sudo apt-get install git-all
sudo wget http://media.steampowered.com/installer/steamcmd_linux.tar.gz
sudo tar -xvzf steamcmd_linux.tar.gz
sudo ./steamcmd.sh +force_install_dir ./l4d2/ +login anonymous +app_update 222860 validate +exit

cd /home/steam/l4d2/left4dead2

git clone https://github.com/altair-sossai/torneio-l4d2-server.git .
```

## Executar o servidor
```bash
sudo screen /home/steam/l4d2/srcds_run -port 27016 -tickrate 100 -secure
```