
# 🔥🐋 Setup Docker Para Projetos Laravel (8 ou 9)

### Passo a passo
1 - Clone Repositório
```sh
git clone https://github.com/elielson-andre/setup-docker-laravel.git
```

2 - Clone os Arquivos do Laravel
```sh
git clone https://github.com/laravel/laravel.git app-laravel
```


3 - Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -rf setup-docker-laravel/* app-laravel/
```
```sh
cd app-laravel/
```


4 - Crie o Arquivo .env
```sh
cp .env.example .env
```


5 - Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=Laravel
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=db_name
DB_USERNAME=root
DB_PASSWORD=pass

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


6 - Suba os containers do projeto
```sh
docker-compose up -d
```


7 - Acessar o container
```sh
docker-compose exec app bash
```


8 - Instalar as dependências do projeto
```sh
composer install
```


9 - Gerar a key do projeto Laravel
```sh
php artisan key:generate
```


10 - Acessar o projeto
[http://localhost:8989](http://localhost:8989)
