# VisualizerPlanilha

Visualizador de panilha

## Bibliotecas necessárias

* Bootstrap 5
* Composer
* PhpSpreadsheet

# Build

## 1. Composer

Para instalar **composer**, inicie o terminal na pasta raiz do projeto: <br>
execute os seguintes comandos no terminal do diretório:

1. Baixa o instalador no diretório

```cmd
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" 
```

2. Verifica o SHA-384 do instalador

```cmd
php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
```

3. Inicia o instalador

```cmd
php composer-setup.php
```

4. Remove o instalador após instalado

```cmd
php -r "unlink('composer-setup.php');"
```

5. Inicializa o composer

```cmd
php composer.phar init
```

## PhpSpreadsheet

Para instalar a biblioteca **phpspreadsheet**, utilize o composer. <br>
Abra o terminal na pasta raiz do projeto:

1. Verifica a versão do composer

```cmd
php composer.phar --version
```

2. Instalar o phpSpreadsheet
```cmd
php composer.phar require phpoffice/phpspreadsheet
```

> [!WARNING]Aviso  
> Caso não consiga instalar o **phpspreadsheet**, verifique se as dependências **ext-gd** e **ext-zip** estão instaladas no php.ini
>
> Para resolver isso, abra o arquivo php.ini, utilize este comando:
> ```cmd 
> php --ini
> ```
>
> Ao executar o comando aparece isso.
> 
> ```
> Configuration File (php.ini) Path: 
> Loaded Configuration File:         C:\xampp\php\php.ini
> Scan for additional .ini files in: (none)
> Additional .ini files parsed:      (none)
> ```
>
> O caminho do arquivo aparace em "**Loaded Configuration File:**" a partir daí, vá a este caminho e abra o arquivo "**php.ini**"
>
> Ao abrir o arquivo, aperte **CTRL + F** e digite "**extension=gd**" e tire o "**;**" no começo. <br>
> Faça isso também com o "**extesion=zip**"
>
> Agora salve o "**php.ini**", agora siga a etapa 2 de instalação do phpSpreadsheet

