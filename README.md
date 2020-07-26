# Descrição

Docker utilizando o compose, arquivo de configuração com variáveis de ambiente e criando um container nginx 1.19.0

# Configuração Container Nginx

1. Exposição de portas

   80 e 443

2. Volume (Obs: verificar se na configuração do docker -> drivers compartilhados, as unidades c: e/ou d: estão habilitadas)

   Aplicação: htdocs -> /usr/share/nginx/html

   Logs: nginx/logs -> /var/log/nginx

   Virtual Host: nginx/sites -> /etc/nginx/conf.d

# Como utitilizar

1. Clone o repositório usando o comando:

   git clone https://gitlab.com/jadilson12/docker-compose-nginx

2. Entre na pasta docker-compose-nginx copie o arquivo env-example para .env.

   cp env-example .env

3. Rode seu container:

   docker-compose up -d

4. Adicione os domínios no arquivo de hosts do windows.

   127.0.0.1 localhost

5) Abra no navegador

   http://localhost

6. Acessar o shell do container:

   winpty docker exec -it nginx bash
