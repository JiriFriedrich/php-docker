# Php project docker starter

## Initial steps:

- create .env file from .env.example and choose a unique project name
- if you don't have nginx-proxy running, delete VIRTUAL_HOST environment variable and uncomment ports section under nginx service
- check if mysql port is available, if not change it respectively
- if you have existing db, put your sql files into .docker/mysql/initdb folder
- put your project files into src folder (main index.php should be inside public dir)
- check .docker/nginx/conf.d/php.conf file and change server_name to your app name
