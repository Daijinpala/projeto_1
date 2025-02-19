<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Ballet:opsz@16..72&display=swap" rel="stylesheet">

<font face="sans-serif"> 
<h1 align="center" style="color: Black;">Configuração de Servidor Web com Monitoramento</h1>
<p align="center">Este projeto tem como objetivo configurar um servidor web na AWS utilizando Nginx, implementar uma página HTML simples e criar um sistema de monitoramento com notificações em caso de indisponibilidade.</p>

<div>
<details>
    <summary style="color: #9400D3; ">Projeto: </summary>
<div>

<h3 style="color: purple;">Parte teorica</h2>

<ol>
<li>Cite 3 exemplos de
distribuição linux.</li>
<li>O que é IP FIXO e sua função.</li>
<li>O que faz o comando ls -la?</li>
<li>o que acontece se eu executar o
comando "shutdown -r -f -t 0" sem ser
root
e sem sudo?</li>
</ol>
</div>

<div>
<h3 style="color: purple;"> Etapa 1: Configuração do Ambiente
</h3>

<div>
<h6> Criar uma VPC na AWS com:</h6>
<ul>
<li> 2 sub-redes públicas (para
acesso externo).</li>
<li> 2 sub-redes privadas (para
futuras expansões).</li>
<li>Uma Internet Gateway conectada
às sub-redes públicas.</li>
</ul>
</div>

<h6>Criar uma instância EC2 na AWS:</h6>

<div>
<ul>
<li> Escolher uma AMI baseada em
Linux (Ubuntu/Debian/Amazon
Linux).</li>
<li>Instalar na sub-rede pública
criada anteriormente.</li>
<li> Associar um Security Group que
permita tráfego HTTP (porta 80) e
SSH (porta 22, opcional).</li>
</ul>
</div>
<h6>Acessar a instância via SSH para
realizar configurações futuras.</h6>
</div>

<div>
<h3 style="color: purple;"> Etapa 2: Configuração do Servidor
</h3>

<div>
<h6>Web
Tarefas:</h6>
<ol>
<li> Instalar o servidor Nginx na EC2.</li>
<li> Criar uma página HTML simples
para ser exibida pelo servidor.</li>
<li> Configurar o Nginx para servir a
página corretamente.</li>
</ol>
</div>

<div>
<ul>
<h6 align="center" style="color: red;">💡 Dicas para os alunos</h6>
<li>Personalizar a página com
informações sobre o projeto.</li>
<li> Criar um serviço systemd para
garantir que o Nginx reinicie
automaticamente se parar.</li>
</ul>
</div>

</div>

<div>
<h3 style="color: purple;"> Etapa 3: Monitoramento e Notificações
Tarefas:
</h3>

<div>
<ol>
<li>Criar um script em Bash ou Python
para monitorar a disponibilidade
do site.</li><br>
<li> O script deve:</li>

<ul>
<li>Verificar se o site responde
corretamente a uma requisição
HTTP.</li>
<li> Criar logs das verificações em
/var/log/monitoramento.log.</li>
<li> Enviar uma notificação via Discord,
Telegram ou Slack se detectar
indisponibilidade.</li>
</ul>

<li> Configurar o script para rodar
automaticamente a cada 1
minuto usando cron ou systemd
timers.
</li>
</ol>
</div>

<div>
<h6 align="center" style="color: red;">💡 Dicas para os alunos</h6>
<ul>
<li>Usar curl no Bash ou requests no
Python para testar a resposta do
site..</li>
<li> Configurar um bot do Telegram
ou webhook do Discord/Slack
para receber alertas..</li>
</ul>
</div>

<div>
<h3 style="color: purple;"> Etapa 4: Automação e Testes
</h3>

<div>
<ol>
<li> Testar a implementação:</li>
<ul>
<li> Verificar se o site está acessível
via navegador.</li>
<li> Parar o Nginx e verificar se o script
detecta e envia alertas
corretamente.</li>
</ul>
<li> Criar uma documentação no
GitHub explicando:
<ul>
<li> Como configurar o ambiente.</li>
<li> Como instalar e configurar o
servidor web.</li>
<li> Como funciona o script de
monitoramento. </li>
<li> Como testar e validar a solução. </li>
</div>

<div>
<h6 align="center" style="color: red;">💡 Dicas para os alunos</h6>
<ul>
<li>Explicar os comandos usados na
documentação</li>
<li> Compartilhar prints dos testes.</li>
</ul>
</div>
</div>
<div>
<h3 align="left" style="color: purple;"> Desafios Bônus</h3>

<div>
<ol>
<li>Automação com User Data:
-Configurar a EC2 para já iniciar
com Nginx, HTML e script de
monitoramento via User Data.</li>
<li> Criação de um template
CloudFormation ou Terraform:
-Criar um arquivo YAML do
CloudFormation que provisiona
toda a infraestrutura
automaticamente.</li>
<li> Monitoramento avançado:
-Enviar estatísticas para
CloudWatch e configurar alarmas
na AWS.</li>
</ol>
</div>

</div>
</div>
</details>

## Resolução:
<div>

<div align="center">
<br>
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Apresenta%C3%A7%C3%A3o"><kbd> <br>Parte Teórica<br> </kbd></a>&ensp; 
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Configurar%20o%20ambiente"><kbd> <br>Configuração do Ambiente<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Intalar%26configurar_ngnix"><kbd> <br>Configuração do Servidor<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/script_monitoramento"><kbd> <br>Monitoramento e Notificações<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/testar%26validar"><kbd> <br>Automação e Testes<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Bonus"><kbd> <br>Bonus<br> </kbd></a>&ensp;&ensp;
<br>

<br><br>
<details align="left">
    <summary style="color: #9400D3;">Estrutura do site HTML:</summary>

```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Configuração de Servidor Web com Monitoramento - Guia completo para configurar e monitorar um servidor web na AWS.">
<meta name="keywords" content="AWS, EC2, Nginx, Monitoramento, Servidor Web, VPC">
<title>Configuração de Servidor Web com Monitoramento</title>
<style>
        body {
            font-family: Arial, sans-serif;
            background-color: #282a36;
            color: #f8f8f2;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #44475a;
            padding: 20px;
            text-align: center;
            color: #f8f8f2;
            font-size: 24px;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #44475a;
                   border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }
        h1, h2 {
            color: #bd93f9;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 5px;
            margin: 10px 0;
            border: 2px solid #6272a4;
        }
        .tips {
            background-color: #6272a4;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .tips p {
            margin: 0;
            color: #f8f8f2;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #44475a;
            color: #f8f8f2;
                    margin-top: 20px;
        }
        a {
            color: #8be9fd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        a:hover {
            color: #ff79c6;
            text-decoration: underline;
        }
        ol, ul {
            color: #f8f8f2;
        }
        @media (max-width: 600px) {
            .container {
                padding: 10px;
            }
            header {
                font-size: 20px;
            }
        }
 </style>
 </head>
 <body>
 <header>
 Configuração de Servidor Web com Monitoramento
 </header>
 <div class="container">
 <h1>Configuração do Ambiente</h1>
 <h2>Tarefas:</h2>
 <ol>
 <li>
 Criar uma VPC na AWS com:
 <ul>
 <li>2 sub-redes públicas (para acesso externo).</li>
 <li>2 sub-redes privadas (para futuras expansões).</li>
 <li>Uma Internet Gateway conectada às sub-redes públicas.</li>
 </ul>
 <img src="1.png" alt="VPC na AWS">
 </li>
 <li>
 Criar uma instância EC2 na AWS:
 <ul>
 <li>Escolher uma AMI baseada em Linux (Ubuntu/Debian/Amazon Linux).</li>
 <li>Instalar na sub-rede pública criada anteriormente.</li>
 <li>Associar um Security Group que permita tráfego HTTP (porta 80) e SSH (porta 22, opcional).</li>
 </ul>
 <img src="2.1.png" alt="Instância EC2">
 <img src="2.2.png" alt="Security Group">
 </li>
 <li>
 Acessar a instância via SSH para realizar configurações futuras.
 <img src="2.3.png" alt="Acesso SSH">
 </li>
 </ol>
  <h1>Configuração do Servidor</h1>
 <h2>Tarefas:</h2>
 <ol>
 <li>
 Instalar o servidor Nginx na EC2.
 <img src="3.png" alt="Instalação do Nginx">
 </li>
 <li>
 Criar uma página HTML simples para ser exibida pelo servidor.
 <pre><code>
 </code></pre>
 </li>
 <li>
 Configurar o Nginx para servir a página corretamente.
 </li>
 </ol>
 <div class="tips">
 <p><strong>Dicas para os alunos:</strong></p>
 <ul>
 <li>Personalizar a página com informações sobre o projeto.</li>
 <li>Criar um serviço systemd para garantir que o Nginx reinicie automaticamente se parar.</li>
 </ul>
 </div>
 <h1>Monitoramento e Notificações</h1>
 <h2>Tarefas:</h2>
 <ol>
 <li>
 Criar um script em Bash ou Python para monitorar a disponibilidade do site.
 </li>
 <li>
 O script deve:
 <ul>
 <li>Verificar se o site responde corretamente a uma requisição HTTP.</li>
 <li>Criar logs das verificações em /var/log/monitoramento.log</li>
 <li>Enviar uma notificação via Discord, Telegram ou Slack se detectar indisponibilidade.</li>
 </ul>
<img src="4.1.png" alt="Script de Monitoramento">
 </li>
<li>
Configurar o script para rodar automaticamente a cada 1 minuto usando cron ou systemd timers.
<img src="4.2.png" alt="Configuração do Cron">
</li>
</ol>
<div class="tips">
<p><strong>Dicas para os alunos:</strong></p>
<ul>
<li>Usar curl no Bash ou requests no Python para testar a resposta do site.</li>
<li>Configurar um bot do Telegram ou webhook do Discord/Slack para receber alertas.</li>
</ul>
</div>
<h1>Automação e Testes</h1>
<h2>Tarefas:</h2>
<ol>
<li>
Testar a implementação:
<ul>
<li>Verificar se o site está acessível via navegador.</li>
<li>Parar o Nginx e verificar se o script detecta e envia alertas corretamente.</li>
</ul>
</li>
<li>
Criar uma documentação no GitHub explicando:
<ul>
<li>Como configurar o ambiente.</li>
<li>Como instalar e configurar o servidor web.</li>
<li>Como funciona o script de monitoramento.</li>
<li>Como testar e validar a solução.</li>
</ul>
</li>
</ol>
<div class="tips">
<p><strong>Dicas para os alunos:</strong></p>
<ul>
<li>Explicar os comandos usados na documentação.</li>
<li>Compartilhar prints dos testes.</li>
</ul>
</div>
<img src="teste1.png" alt="Teste 1">
<img src="teste2.png" alt="Teste 2">
<img src="teste3.png" alt="Teste 3">
<div class="tips">
<p><strong>Repositório do GitHub:</strong></p>
<p>
Acesse o repositório do projeto no GitHub para ver a documentação completa e o código-fonte:
<a href="https://github.com/Daijinpala/projeto_1.git" target="_blank">GitHub - Projeto 1</a>
</p>
</div>
</div>
<footer>
&copy; 2025 - Configuração de Servidor Web com Monitoramento |
<a  href="https://github.com/Daijinpala/projeto_1.git" target="_blank">Repositório no GitHub</a>
</footer>
</body>
</html>
```
</details>

<br>

<details align="left">
    <summary style="color: #9400D3;">Estrutura GitHub: </summary>

```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Ballet:opsz@16..72&display=swap" rel="stylesheet">

<font face="sans-serif"> 
<h1 align="center" style="color: Black;">Configuração de Servidor Web com Monitoramento</h1>
<p align="center">Este projeto tem como objetivo configurar um servidor web na AWS utilizando Nginx, implementar uma página HTML simples e criar um sistema de monitoramento com notificações em caso de indisponibilidade.</p>

<div>
<details>
    <summary style="color: #9400D3; ">Projeto</summary>
<div>

<h3 style="color: purple;">Parte teorica</h2>

<ol>
<li>Cite 3 exemplos de
distribuição linux.</li>
<li>O que é IP FIXO e sua função.</li>
<li>O que faz o comando ls -la?</li>
<li>o que acontece se eu executar o
comando "shutdown -r -f -t 0" sem ser
root
e sem sudo?</li>
</ol>
</div>

<div>
<h3 style="color: purple;"> Etapa 1: Configuração do Ambiente
</h3>

<div>
<h6> Criar uma VPC na AWS com:</h6>
<ul>
<li> 2 sub-redes públicas (para
acesso externo).</li>
<li> 2 sub-redes privadas (para
futuras expansões).</li>
<li>Uma Internet Gateway conectada
às sub-redes públicas.</li>
</ul>
</div>

<h6>Criar uma instância EC2 na AWS:</h6>

<div>
<ul>
<li> Escolher uma AMI baseada em
Linux (Ubuntu/Debian/Amazon
Linux).</li>
<li>Instalar na sub-rede pública
criada anteriormente.</li>
<li> Associar um Security Group que
permita tráfego HTTP (porta 80) e
SSH (porta 22, opcional).</li>
</ul>
</div>
<h6>Acessar a instância via SSH para
realizar configurações futuras.</h6>
</div>

<div>
<h3 style="color: purple;"> Etapa 2: Configuração do Servidor
</h3>

<div>
<h6>Web
Tarefas:</h6>
<ol>
<li> Instalar o servidor Nginx na EC2.</li>
<li> Criar uma página HTML simples
para ser exibida pelo servidor.</li>
<li> Configurar o Nginx para servir a
página corretamente.</li>
</ol>
</div>

<div>
<ul>
<h6 align="center" style="color: red;">💡 Dicas para os alunos</h6>
<li>Personalizar a página com
informações sobre o projeto.</li>
<li> Criar um serviço systemd para
garantir que o Nginx reinicie
automaticamente se parar.</li>
</ul>
</div>

</div>

<div>
<h3 style="color: purple;"> Etapa 3: Monitoramento e Notificações
Tarefas:
</h3>

<div>
<ol>
<li>Criar um script em Bash ou Python
para monitorar a disponibilidade
do site.</li><br>
<li> O script deve:</li>

<ul>
<li>Verificar se o site responde
corretamente a uma requisição
HTTP.</li>
<li> Criar logs das verificações em
/var/log/monitoramento.log.</li>
<li> Enviar uma notificação via Discord,
Telegram ou Slack se detectar
indisponibilidade.</li>
</ul>

<li> Configurar o script para rodar
automaticamente a cada 1
minuto usando cron ou systemd
timers.
</li>
</ol>
</div>

<div>
<h6 align="center" style="color: red;">💡 Dicas para os alunos</h6>
<ul>
<li>Usar curl no Bash ou requests no
Python para testar a resposta do
site..</li>
<li> Configurar um bot do Telegram
ou webhook do Discord/Slack
para receber alertas..</li>
</ul>
</div>

<div>
<h3 style="color: purple;"> Etapa 4: Automação e Testes
</h3>

<div>
<ol>
<li> Testar a implementação:</li>
<ul>
<li> Verificar se o site está acessível
via navegador.</li>
<li> Parar o Nginx e verificar se o script
detecta e envia alertas
corretamente.</li>
</ul>
<li> Criar uma documentação no
GitHub explicando:
<ul>
<li> Como configurar o ambiente.</li>
<li> Como instalar e configurar o
servidor web.</li>
<li> Como funciona o script de
monitoramento. </li>
<li> Como testar e validar a solução. </li>
</div>

<div>
<h6 align="center" style="color: red;">💡 Dicas para os alunos</h6>
<ul>
<li>Explicar os comandos usados na
documentação</li>
<li> Compartilhar prints dos testes.</li>
</ul>
</div>
</div>
<div>
<h3 align="left" style="color: purple;"> Desafios Bônus</h3>

<div>
<ol>
<li>Automação com User Data:
-Configurar a EC2 para já iniciar
com Nginx, HTML e script de
monitoramento via User Data.</li>
<li> Criação de um template
CloudFormation ou Terraform:
-Criar um arquivo YAML do
CloudFormation que provisiona
toda a infraestrutura
automaticamente.</li>
<li> Monitoramento avançado:
-Enviar estatísticas para
CloudWatch e configurar alarmas
na AWS.</li>
</ol>
</div>

</div>
</div>
</details>

## Resolução:
<div>

<div align="center">
<br>
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Configurar%20o%20ambiente"><kbd> <br>Configuração do Ambiente<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Intalar%26configurar_ngnix"><kbd> <br>Configuração do Servidor<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/script_monitoramento"><kbd> <br>Monitoramento e Notificações<br> </kbd></a>&ensp;&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/testar%26validar"><kbd> <br>Automação e Testes<br> </kbd></a>&ensp;&ensp;
  <a href=""><kbd> <br>Bonus<br> </kbd></a>&ensp;&ensp;
<br>

<br><br>
<details align="left">
    <summary style="color: #9400D3;">Estrutura do site HTML:</summary>

<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Configuração de Servidor Web com Monitoramento - Guia completo para configurar e monitorar um servidor web na AWS.">
<meta name="keywords" content="AWS, EC2, Nginx, Monitoramento, Servidor Web, VPC">
<title>Configuração de Servidor Web com Monitoramento</title>
<style>
        body {
            font-family: Arial, sans-serif;
            background-color: #282a36;
            color: #f8f8f2;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #44475a;
            padding: 20px;
            text-align: center;
            color: #f8f8f2;
            font-size: 24px;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #44475a;
                   border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        }
        h1, h2 {
            color: #bd93f9;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 5px;
            margin: 10px 0;
            border: 2px solid #6272a4;
        }
        .tips {
            background-color: #6272a4;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .tips p {
            margin: 0;
            color: #f8f8f2;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #44475a;
            color: #f8f8f2;
                    margin-top: 20px;
        }
        a {
            color: #8be9fd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        a:hover {
            color: #ff79c6;
            text-decoration: underline;
        }
        ol, ul {
            color: #f8f8f2;
        }
        @media (max-width: 600px) {
            .container {
                padding: 10px;
            }
            header {
                font-size: 20px;
            }
        }
 </style>
 </head>
 <body>
 <header>
 Configuração de Servidor Web com Monitoramento
 </header>
 <div class="container">
 <h1>Configuração do Ambiente</h1>
 <h2>Tarefas:</h2>
 <ol>
 <li>
 Criar uma VPC na AWS com:
 <ul>
 <li>2 sub-redes públicas (para acesso externo).</li>
 <li>2 sub-redes privadas (para futuras expansões).</li>
 <li>Uma Internet Gateway conectada às sub-redes públicas.</li>
 </ul>
 <img src="1.png" alt="VPC na AWS">
 </li>
 <li>
 Criar uma instância EC2 na AWS:
 <ul>
 <li>Escolher uma AMI baseada em Linux (Ubuntu/Debian/Amazon Linux).</li>
 <li>Instalar na sub-rede pública criada anteriormente.</li>
 <li>Associar um Security Group que permita tráfego HTTP (porta 80) e SSH (porta 22, opcional).</li>
 </ul>
 <img src="2.1.png" alt="Instância EC2">
 <img src="2.2.png" alt="Security Group">
 </li>
 <li>
 Acessar a instância via SSH para realizar configurações futuras.
 <img src="2.3.png" alt="Acesso SSH">
 </li>
 </ol>
  <h1>Configuração do Servidor</h1>
 <h2>Tarefas:</h2>
 <ol>
 <li>
 Instalar o servidor Nginx na EC2.
 <img src="3.png" alt="Instalação do Nginx">
 </li>
 <li>
 Criar uma página HTML simples para ser exibida pelo servidor.
 <pre><code>
 </code></pre>
 </li>
 <li>
 Configurar o Nginx para servir a página corretamente.
 </li>
 </ol>
 <div class="tips">
 <p><strong>Dicas para os alunos:</strong></p>
 <ul>
 <li>Personalizar a página com informações sobre o projeto.</li>
 <li>Criar um serviço systemd para garantir que o Nginx reinicie automaticamente se parar.</li>
 </ul>
 </div>
 <h1>Monitoramento e Notificações</h1>
 <h2>Tarefas:</h2>
 <ol>
 <li>
 Criar um script em Bash ou Python para monitorar a disponibilidade do site.
 </li>
 <li>
 O script deve:
 <ul>
 <li>Verificar se o site responde corretamente a uma requisição HTTP.</li>
 <li>Criar logs das verificações em /var/log/monitoramento.log</li>
 <li>Enviar uma notificação via Discord, Telegram ou Slack se detectar indisponibilidade.</li>
 </ul>
<img src="4.1.png" alt="Script de Monitoramento">
 </li>
<li>
Configurar o script para rodar automaticamente a cada 1 minuto usando cron ou systemd timers.
<img src="4.2.png" alt="Configuração do Cron">
</li>
</ol>
<div class="tips">
<p><strong>Dicas para os alunos:</strong></p>
<ul>
<li>Usar curl no Bash ou requests no Python para testar a resposta do site.</li>
<li>Configurar um bot do Telegram ou webhook do Discord/Slack para receber alertas.</li>
</ul>
</div>
<h1>Automação e Testes</h1>
<h2>Tarefas:</h2>
<ol>
<li>
Testar a implementação:
<ul>
<li>Verificar se o site está acessível via navegador.</li>
<li>Parar o Nginx e verificar se o script detecta e envia alertas corretamente.</li>
</ul>
</li>
<li>
Criar uma documentação no GitHub explicando:
<ul>
<li>Como configurar o ambiente.</li>
<li>Como instalar e configurar o servidor web.</li>
<li>Como funciona o script de monitoramento.</li>
<li>Como testar e validar a solução.</li>
</ul>
</li>
</ol>
<div class="tips">
<p><strong>Dicas para os alunos:</strong></p>
<ul>
<li>Explicar os comandos usados na documentação.</li>
<li>Compartilhar prints dos testes.</li>
</ul>
</div>
<img src="teste1.png" alt="Teste 1">
<img src="teste2.png" alt="Teste 2">
<img src="teste3.png" alt="Teste 3">
<div class="tips">
<p><strong>Repositório do GitHub:</strong></p>
p>
Acesse o repositório do projeto no GitHub para ver a documentação completa e o código-fonte:
<a href="https://github.com/Daijinpala/projeto_1.git" target="_blank">GitHub - Projeto 1</a>
</p>
</div>
</div>
<footer>
&copy; 2025 - Configuração de Servidor Web com Monitoramento |
<a  href="https://github.com/Daijinpala/projeto_1.git" target="_blank">Repositório no GitHub</a>
</footer>
</body>
</html>

</details>

<br>

<br>

## Sites utilizados como referencia:

> Básico shell: https://diegomariano.com/shell-script-um-guia-basico/<p></p>

> GODSCRIPT: https://devhints.io/bash<p></p>

>Discord Webhooks: https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks

>Fontes de letra: https://www.futuraexpress.com.br/blog/fontes-de-letras-diferentes/

>Solução de problemas: https://stackexchange.com/

>Exportação da fonte:  https://fonts.google.com/ 

<p align="center">O projeto inteiro está zipado, abrir com o obsidian para ter uma melhor vizualização!</p>
</font>

<h2 align="center">Integrantes:</h2>

<font face="Ballet" style="color: #9400D3;">
<footer>
<p style = 'font-size:60px'>
Flávio Cavalcante
<br>
Bruno Bacchi
<br>
Afonso Luiz
<br>
</p>
</footer>
</font>
```

</details>

<br>

## Sites utilizados como referencia:

> Básico shell: https://diegomariano.com/shell-script-um-guia-basico/<p></p>

> GODSCRIPT: https://devhints.io/bash<p></p>

>Discord Webhooks: https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks

>Fontes de letra: https://www.futuraexpress.com.br/blog/fontes-de-letras-diferentes/

>Solução de problemas: https://stackexchange.com/

>Exportação da fonte:  https://fonts.google.com/

>tutorial terraform(base):https://www.youtube.com/watch?v=bIPF_hzmQGE&list=PLWQmZVQayUUIgSmOj3GPH2BJcn0hOzIaP&index=2&ab_channel=CleberGasparoto

>comando curl(base):https://www.hostinger.com.br/tutoriais/comando-curl-linux 

<p align="center">O projeto inteiro está zipado, abrir com o obsidian para ter uma melhor vizualização!</p>
</font>

<h2 align="center">Integrantes:</h2>

<font face="Ballet" style="color: #9400D3;">
<footer>
<p style = 'font-size:60px'>
<br>
Afonso Luiz
<br>
Bruno Bacchi
<br>
Flávio Cavalcante
<br>
</p>
</footer>
</font>
