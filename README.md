# mercadinho-PGE

Para replicar o projeto no seu ambiente precisamos ter o docker e docker-compose instalados e funcionado em seu ambiente de desenvolvimento.

Após fazer o clone do projeto precisamos criar um arquivo .env, vamos aproveitar o arquivo .env.exemplo e renomear para .env .
Temos um arquivo env que guarda os acesso ao banco de dados basta voce colocar no seu .env ficando desse jeito 
DB_CONNECTION=pgsql
DB_HOST=postgres
DB_PORT=5432
DB_DATABASE=db
DB_USERNAME=dev
DB_PASSWORD=secret

Agora vamos instalar as dependencias, precisamos estar dentro do diretorio que contem o arquivo docker-compose.yaml, execute o seguinte comando " docker-compose run web composer install " vai instalar todas as dependencias necessarias para o funcionamento do projeto.

Precisamos criar a APP_key do .env com o comando  " docker-compose run web php artisan key generate " .

Caso todos os passo tenham dado certo vamos subir nossa aplicação com "docker-compose up", esse comando vai fazer a criação dos container e redes descritos no arquivo docker-compose.yaml
