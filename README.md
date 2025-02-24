# Configuração de Servidor Web com Monitoramento

Este projeto tem como objetivo configurar um servidor web na AWS utilizando Nginx, implementar uma página HTML simples e criar um sistema de monitoramento com notificações em caso de indisponibilidade.

---

## Aplicações utilizadas:

### GitHub, Amazon Web Services, Microsoft Store, WSL, Visual Studio Code, Nginx.

<div align="center">
  <br>
  <a href="https://github.com/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/gitlogo.png" alt="GitHub" width="150">
  </a>&ensp;

  <a href="https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwjKuL74ltWLAxXoEUQIHY40KqwYABAAGgJkeg&co=1&ase=2&gclid=CjwKCAiA5eC9BhAuEiwA3CKwQp-uZ-EhfKVs_yaTVCZmvhF8olLyCz4sF_rQXc-KTkKjJ6zjkq_KbRoCmx0QAvD_BwE&ei=46i4Z7zJLbLb5OUP_NnOYQ&ohost=www.google.com&cid=CAESVeD2mSl7f0Xe0yyJImaMygYDsAuUvVqE8TXk7HbEuO8df6HhHkyj13nbeuQIUd6NDilzCovM3hpvmJWnXIKlBj1rDcr0Uva9DVYGZCTyi2T-YG-tn0A&sig=AOD64_3dqO5hHHx21zCm5ROWF8TSPV62pA&q&sqi=2&nis=4&adurl&ved=2ahUKEwj8xrT4ltWLAxWyLbkGHfysMwwQ0Qx6BAgIEAE">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/amazonlogo.png" alt="Amazon Web Services" width="150" height="150">
  </a>&ensp;

  <a href="https://apps.microsoft.com/home?hl=pt-BR&gl=BR">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/micstorelogo.png" alt="Microsoft Store" width="150" height="150">
  </a>&ensp;

  <a href="https://www.microsoft.com/store/productId/9P9TQF7MRM4R?ocid=libraryshare">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/wsllogo.png" alt="WSL" width="150" height="150">
  </a>&ensp;

  <a href="https://code.visualstudio.com/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/vscodelogo.png" alt="Visual Studio Code" width="150" height="150">
  </a>&ensp;

  <a href="https://nginx.org/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/nginxlogo.png" alt="Nginx" width="150" height="150">
  </a>&ensp;
</div>

> [!IMPORTANT]
> As únicas aplicações específicas que se pede a utilização no projeto são o **GitHub** e o **Amazon Web Services**. As outras foram questão de preferência!

> [!TIP]
> - **GitHub:** Utilizado para a documentação do projeto.
> - **Amazon Web Services (AWS):** Utilizado para a criação da infraestrutura de TI.
> - **Microsoft Store:** Utilizado para baixar o WSL e o Ubuntu 24.04.
> - **WSL (Windows Subsystem for Linux):** Permite executar um ambiente Linux diretamente no sistema operacional Windows.
> - **Visual Studio Code:** Utilizado como editor de código e terminal.
> - **Nginx:** Utilizado como servidor web.

---

## Linguagens utilizadas:

### Bash, Markdown.

<div align="left">
  <br>
  <a href="https://www.gnu.org/software/bash/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/bashlogo.jpeg" alt="Bash" width="150" height="150">
  </a>&ensp;

  <a href="https://www.markdownguide.org/">
    <img src="https://github.com/Daijinpala/projeto_1/blob/main/logo/marklogo.png" alt="Markdown" width="150" height="150">
  </a>&ensp;
</div>

> [!IMPORTANT]
> Você pode utilizar a linguagem Python ao invés de Bash.

> [!TIP]
> - **Bash:** É uma linguagem de script e um interpretador de comandos.
> - **Markdown:** É uma linguagem de marcação leve.

---

## Projeto:

### Parte teórica

1. Cite 3 exemplos de distribuição Linux.
2. O que é IP FIXO e sua função.
3. O que faz o comando `ls -la`?
4. O que acontece se eu executar o comando `shutdown -r -f -t 0` sem ser root e sem sudo?

### Etapa 1: Configuração do Ambiente

#### Criar uma VPC na AWS com:

- 2 sub-redes públicas (para acesso externo).
- 2 sub-redes privadas (para futuras expansões).
- Uma Internet Gateway conectada às sub-redes públicas.

#### Criar uma instância EC2 na AWS:

- Escolher uma AMI baseada em Linux (Ubuntu/Debian/Amazon Linux).
- Instalar na sub-rede pública criada anteriormente.
- Associar um Security Group que permita tráfego HTTP (porta 80) e SSH (porta 22, opcional).

#### Acessar a instância via SSH para realizar configurações futuras.

### Etapa 2: Configuração do Servidor Web

#### Tarefas:

1. Instalar o servidor Nginx na EC2.
2. Criar uma página HTML simples para ser exibida pelo servidor.
3. Configurar o Nginx para servir a página corretamente.

#### 💡 Dicas para os alunos

- Personalizar a página com informações sobre o projeto.
- Criar um serviço systemd para garantir que o Nginx reinicie automaticamente se parar.

### Etapa 3: Monitoramento e Notificações

#### Tarefas:

1. Criar um script em Bash ou Python para monitorar a disponibilidade do site.
2. O script deve:
   - Verificar se o site responde corretamente a uma requisição HTTP.
   - Criar logs das verificações em `/var/log/monitoramento.log`.
   - Enviar uma notificação via Discord, Telegram ou Slack se detectar indisponibilidade.
3. Configurar o script para rodar automaticamente a cada 1 minuto usando cron ou systemd timers.

#### 💡 Dicas para os alunos

- Usar `curl` no Bash ou `requests` no Python para testar a resposta do site.
- Configurar um bot do Telegram ou webhook do Discord/Slack para receber alertas.

### Etapa 4: Automação e Testes

#### Tarefas:

1. Testar a implementação:
   - Verificar se o site está acessível via navegador.
   - Parar o Nginx e verificar se o script detecta e envia alertas corretamente.
2. Criar uma documentação no GitHub explicando:
   - Como configurar o ambiente.
   - Como instalar e configurar o servidor web.
   - Como funciona o script de monitoramento.
   - Como testar e validar a solução.

#### 💡 Dicas para os alunos

- Explicar os comandos usados na documentação.
- Compartilhar prints dos testes.

### Desafios Bônus

1. Automação com User Data:
   - Configurar a EC2 para já iniciar com Nginx, HTML e script de monitoramento via User Data.
2. Criação de um template CloudFormation ou Terraform:
   - Criar um arquivo YAML do CloudFormation que provisiona toda a infraestrutura automaticamente.
3. Monitoramento avançado:
   - Enviar estatísticas para CloudWatch e configurar alarmas na AWS.

---
## Resolução:

<div align="center">
  <br>
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Apresenta%C3%A7%C3%A3o"><kbd> <br>Parte Teórica<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Configurar%20o%20ambiente"><kbd> <br>Configuração do Ambiente<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Intalar%26configurar_ngnix"><kbd> <br>Configuração do Servidor<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/script_monitoramento"><kbd> <br>Monitoramento e Notificações<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/testar%26validar"><kbd> <br>Automação e Testes<br> </kbd></a>&ensp;
  <a href="https://github.com/Daijinpala/projeto_1/tree/main/Bonus"><kbd> <br>Bonus<br> </kbd></a>&ensp;
  <br>
</div>
<br>
<br>

> [!NOTE]
> Cada botão te levará para a resolução de uma determinada parte do projeto de mesmo nome!

---

## Sites utilizados como referência:

- Básico shell: https://diegomariano.com/shell-script-um-guia-basico/
- GODSCRIPT: https://devhints.io/bash
- Discord Webhooks: https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks
- Fontes de letra: https://www.futuraexpress.com.br/blog/fontes-de-letras-diferentes/
- Solução de problemas: https://stackexchange.com/
- Exportação da fonte: https://fonts.google.com/
- Tutorial terraform(base): https://www.youtube.com/watch?v=bIPF_hzmQGE&list=PLWQmZVQayUUIgSmOj3GPH2BJcn0hOzIaP&index=2&ab_channel=CleberGasparoto
- Comando curl(base): https://www.hostinger.com.br/tutoriais/comando-curl-linux
- Sintaxe GitHub(base): https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

<p align="center">O projeto inteiro está zipado, abrir com o Obsidian para ter uma melhor visualização!(Falta att.)</p>

---

## Integrantes:

<font face="Ballet" style="color: #9400D3;">
<footer>
<p style="font-size:60px">

<p align="center">Afonso Luiz</p>

<p align="center">Bruno Bacchi</p>

<p align="center">Flávio Cavalcante</p>
</p>
</footer>
</font>
