# Construindo o seu ambiente de desenvolvimento Laravel com Docker
Este repositório tem as configurações de instalação do Laravel para usar o Docker em ambiente de desenvolvimento. Este repositório pode ser usado como ponto de partida para o desenvolvimento de aplicativos Laravel com o Docker.

# Instalação do Docker

Não vou estrar como instalar o Docker porque no youtube tem vários tutoriais excelente pra isso:

 - [Instalar no Windows](https://youtu.be/OweZAewo54A)
 - [Instalar no Linux](https://youtu.be/C8jlT8jhL3g)
 - [Instalar no Mac](https://youtu.be/nbtuXPRedos)

Esta configuração contém:

 - PHP-FPM (PHP 7)
 - PHPMyAdmin
 - Composer 
 - Nginx web server
 - MySQL database

## Instalaçao
  Certifique-se que a instalação do [Docker](https://hub.docker.com/_/hello-world) ocorreu perfeitamente.

  Clone o repositório
  ```sh
  git clone https://github.com/ReinanHS/docker-laravel.git
  ```
  Alterar o diretório
  ```sh
    cd docker-laravel
  ```
  Agora vamos criar o projeto laravel em SRC
  ```sh
    cd src && composer install
  ```
  Crie e execute os contêineres do Docker
  ```sh
    docker-compose up -d
  ```
  Para pausar todos os contêineres é só executar
  ```sh
    docker stop $(docker ps -a -q)
   ```
  
  Para pegar o IP do seu contêiner use:
  ´´´sh
  docker-machine ip 
  ´´´
  ou
  ´´´sh
  ipconfig
  ´´´
