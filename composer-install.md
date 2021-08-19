**Instalar composer (MacOS)**


Executar respectivamente no terminal:

1. `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`
2. `php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') {  echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"`
3. `php composer-setup.php`
4. `php -r "unlink('composer-setup.php');"`
5. `sudo mv composer.phar /usr/local/bin/composer`
  
   
**Iniciar composer no projeto PHP**

Na raiz do projeto, digite: `composer init` (resposta as perguntas até finalizar)

_Instalar autoload_

1. Digite para instalar: `composer dump-autoload`
2. Adicione em _composer.json_ o seguinte código: 
  `"autoload": {
     "psr-4": {
          "MyDir\\": "src/"
      },
   },`
    
   
**Observaçōes**

1. Sempre que precisar instalar dependência: `composer require nome-dependencia`
2. Sempre que precisar atualizar todas as dependências: `composer update`

 
**Pacotes úteis**

- `composer require components/jquery`
- `composer require blueimp/jquery-file-upload`
- `composer phpmailer/phpmailer`

 
Fonte: https://getcomposer.org/download/
