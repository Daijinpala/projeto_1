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

<h3 style="color: purple;">Parte teórica</h2>

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
<br>

# Aplicações utilizadas
<h2>Github, Amazon Web Services, Microsoft Store, WSL, Visual Studio Code, Nginx.</h2>

<div align="center">
  <br>
  <a href="https://github.com/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/gitlogo.png" alt="GitHub" width="150">
  </a>&ensp;

  <a href="https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwjKuL74ltWLAxXoEUQIHY40KqwYABAAGgJkeg&co=1&ase=2&gclid=CjwKCAiA5eC9BhAuEiwA3CKwQp-uZ-EhfKVs_yaTVCZmvhF8olLyCz4sF_rQXc-KTkKjJ6zjkq_KbRoCmx0QAvD_BwE&ei=46i4Z7zJLbLb5OUP_NnOYQ&ohost=www.google.com&cid=CAESVeD2mSl7f0Xe0yyJImaMygYDsAuUvVqE8TXk7HbEuO8df6HhHkyj13nbeuQIUd6NDilzCovM3hpvmJWnXIKlBj1rDcr0Uva9DVYGZCTyi2T-YG-tn0A&sig=AOD64_3dqO5hHHx21zCm5ROWF8TSPV62pA&q&sqi=2&nis=4&adurl&ved=2ahUKEwj8xrT4ltWLAxWyLbkGHfysMwwQ0Qx6BAgIEAE">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/amazonlogo.png" alt="Amazon Web Services
" width="150" height = "150">
  </a>&ensp;

 <a href="https://apps.microsoft.com/home?hl=pt-BR&gl=BR">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/micstorelogo.png" alt="Microsoft Store
" width="150" height = "150">
  </a>&ensp;

  <a href="https://www.microsoft.com/store/productId/9P9TQF7MRM4R?ocid=libraryshare">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/wsllogo.png" alt="WSL" width="150" height = "150">
  </a>&ensp;
 
  <a href="https://code.visualstudio.com/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/vscodelogo.png" alt="Visual Studio Code" width="150" height = "150">
  </a>&ensp;

  <a href="https://nginx.org/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/nginxlogo.png" alt="Nginx" width="150" height = "150">
  </a>&ensp;
</div>
<br><br>

> [!IMPORTANT]
> As únicas aplicações específicas que se pede a utilização no projeto são o **GitHub** e o **Amazon Web Services**. As outras foram questão de preferência!

> [!TIP]
> - **GitHub:** Utilizado para a documentação do projeto.
> - **Amazon Web Services (AWS):** Utilizado para a criação da infraestrutura de TI.
> - **Microsoft Store:** Utilizado para baixar o WSL e o Ubuntu 24.04.
> - **WSL (Windows Subsystem for Linux):** Permite executar um ambiente Linux diretamente no sistema operacional Windows.
> - **Visual Studio Code:** Utilizado como editor de código e terminal.
> - **Nginx:** Utilizado como servidor web.

# Linguagens utilizadas

<h2>Bash, Markdown.</h2>

<div align="center">
  <br>
  <a href="https://www.gnu.org/software/bash/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/bashlogo.jpeg" alt="Bash" width="150" height = "150">
  </a>&ensp;

  <a href="https://www.markdownguide.org/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/marklogo.png" alt="Markdown" width="150" height = "150">
  </a>&ensp;


 <br>
</div>

## Resolução:
<div>

<div align="center">
<br>
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Apresenta%C3%A7%C3%A3o"><kbd> <br>Parte Teórica<br> </kbd></a>&ensp; 
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Configurar%20o%20ambiente"><kbd> <br>Configuração do Ambiente<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Intalar%26configurar_ngnix"><kbd> <br>Configuração do Servidor<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/script_monitoramento"><kbd> <br>Monitoramento e Notificações<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/testar%26validar"><kbd> <br>Automação e Testes<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Bonus"><kbd> <br>Bonus<br> </kbd></a>&ensp;
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

>Básico shell: https://diegomariano.com/shell-script-um-guia-basico/<br>
>GODSCRIPT: https://devhints.io/bash<br>
>Discord Webhooks: https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks<br>
>Fontes de letra: https://www.futuraexpress.com.br/blog/fontes-de-letras-diferentes/<br>
>Solução de problemas: https://stackexchange.com/<br>
>Exportação da fonte:  https://fonts.google.com/<br>
>Tutorial terraform(base):https://www.youtube.com/watch?v=bIPF_hzmQGE&list=PLWQmZVQayUUIgSmOj3GPH2BJcn0hOzIaP&index=2&ab_channel=CleberGasparoto<br>
>Comando curl(base):https://www.hostinger.com.br/tutoriais/comando-curl-linux <br>
>Sintaxe GitHub(base): https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax<br>

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
