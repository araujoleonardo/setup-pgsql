## Setup Laravel Docker

### Laravel ^10.10
### PHP ^8.2
### Postgresql ^12.17
### Tailwind ^2.2.7

1. Clone o resitorio do github.</br></br>
```
git clone repositorio-do-github
```

2. Acesse a pasta do repositorio clonado.</br></br>
```
cd meu-site
```

3. Cria uma copia do arquivo .env.example.</br></br>
```
cp .env.example .env
```

4. Abra o arquivo .env criado.</br></br>
```
vim .env
```

5. Altere as linhas necessárias.</br></br>
```
DB_CONNECTION=postgres
DB_HOST=postgres
DB_PORT=5432
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

PGADMIN_DEFAULT_EMAIL=teste@gmail.com
PGADMIN_DEFAULT_PASSWORD=teste
```

6. Saia do editor e salve as alterações.</br></br>

7. Crie os container no docker.</br></br>
```
docker-compose up
```

8. Abra o container da aplicação e instale todas as dependências do laravel.</br></br>
```
composer install
```

9. Defina a APP_KEY do arquivo .env .</br></br>
```
php artisan key:generate
```

10. Faça a migração de todas as tabelas do banco.</br></br>
```
php artisan migrate
```
