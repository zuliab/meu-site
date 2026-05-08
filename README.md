# Projeto Vagrant + Apache
# Objetivo
Este projeto cria uma máquina virtual Debian utilizando Vagrant e VirtualBox para hospedar um site simples com Apache2.

# O que foi configurado
Utilização da box cloud-image/debian-13
Criação da VM com 1GB de memória
Redirecionamento da porta 8080 do host para a porta 80 da VM
Redirecionamento da porta 2222 para acesso SSH
Configuração de rede privada com IP 192.168.0.2
Compartilhamento da pasta ./meu-site com /var/www/meu-site
Instalação automática do Apache2 via provisionamento Shell
Configuração do Apache para servir os arquivos da pasta compartilhada
# Acesso
Site
http://localhost:8080
SSH
vagrant ssh
# Tecnologias utilizadas
Vagrant
VirtualBox
Debian 13
Apache2
Shell Script